# WooCommerce Product Sayısı

```javascript
jQuery(document).ready(function($) {
    $('.stock').each(function() {
        var stockText = $(this).text().match(/\d+/);
        if (stockText && parseInt(stockText[0]) > 10) {
            $(this).text('10+');
        }
    });
});
```

## Yıl Alma HTML Bloğu

```html
<a href="https://a8.com.tr"><strong>A8 Bilişim Ar-Ge Team</strong>©
<span id="yil"></span></a> 
<script>
document.getElementById('yil').textContent = new Date().getFullYear();
</script>
```
