# Admin Koli Adeti Kaydet

## Kod

```php
add_action('woocommerce_admin_process_product_object', function ($product) {

    if (isset($_POST['_koli_adedi'])) {
        $koli_adedi = max(1, intval($_POST['_koli_adedi']));
        $product->update_meta_data('_koli_adedi', $koli_adedi);
    }
});

//Varyasyonlu ürünlerde kaydet
add_action('woocommerce_save_product_variation', 'save_koli_adedi_variations', 10, 2);
function save_koli_adedi_variations($variation_id, $i) {

    if (isset($_POST['_koli_adedi'][$i])) {
        $koli_adedi = max(1, intval($_POST['_koli_adedi'][$i]));
        update_post_meta($variation_id, '_koli_adedi', $koli_adedi);
    }
}
```
