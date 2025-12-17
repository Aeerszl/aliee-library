# Sepete Ekle Butonundan Önce Koli Adet Fiyatı İbaresi

## Önizleme
![Koli Bilgisi Önizleme](images/lib-1   sepetönce.png)

## Kod

```php
add_action('woocommerce_single_product_summary', 'woodmart_koli_info', 25);
function woodmart_koli_info() {
    global $product;

    if (!$product) return;

    $koli_adedi = 8; // default

    // Varyasyonlu ürünse → ilk varyasyonu al
    if ($product->is_type('variable')) {
        $variations = $product->get_available_variations();
        if (!empty($variations)) {
            $first_variation_id = $variations[0]['variation_id'];
            $meta = get_post_meta($first_variation_id, '_koli_adedi', true);
            if ($meta > 0) {
                $koli_adedi = (int) $meta;
            }
        }
    } else {
        // Basit ürün
        $meta = $product->get_meta('_koli_adedi');
        if ($meta > 0) {
            $koli_adedi = (int) $meta;
        }
    }

    echo '<div class="koli-info" style="margin:10px 0;font-weight:600;">
        📦 1 Koli = ' . esc_html($koli_adedi) . ' Adet Üründen Oluşur.<br>
        Perakende Satışımız Yoktur.
    </div>';
}
add_filter('woocommerce_available_variation', function ($variation) {
    $koli = get_post_meta($variation['variation_id'], '_koli_adedi', true);
    $variation['koli_adedi'] = $koli ? (int)$koli : 8;
    return $variation;
});

add_action('wp_footer', function () {
    if (!is_product()) return;
    ?>
    <script>
    jQuery(function ($) {
        $('form.variations_form').on('found_variation', function (e, variation) {
            if (variation.koli_adedi) {
                $('.koli-info').html(
                    '📦 1 Koli = ' + variation.koli_adedi + ' Adet Üründen Oluşur.<br>Perakende Satışımız Yoktur.'
                );
            }
        });
    });
    </script>
    <?php
});
```
