# Disable Admin Bar

## Açıklama
Sayfanın üstündeki siyah admin panelini kaldırır

## Kod

```php
add_action( 'wp', function () {
	if ( ! current_user_can( 'manage_options' ) ) {
		show_admin_bar( false );
	}
} );
```
