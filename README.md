# inpsyde-wp-nonce

## Installation
```shell
	composer require inpsyde-wp-nonce/wp-nonce-oo
```

## How to use

Create nonce
```php
	$nonce = \Inpsyde\Nonce::wp_create_nonce();
```

Verify nonce
```php
	$isValid = \Inpsyde\Nonce::wp_verify_nonce($nonce);
```

Create nonce hidden input
```php
	\Inpsyde\Nonce::wp_nonce_field();
```

Generate nonce URL:
```php
	$url = \Inpsyde\Nonce::wp_nonce_url('http://www.google.com');
```

Check if request was been referred from an admin screen:
```php
	$admin = \Inpsyde\Nonce::check_admin_referer();
```

Verifies the AJAX request to prevent processing requests external of the blog.
```php
	$ajax = \Inpsyde\Nonce::check_ajax_referer();
```

## Testing
```shell
vendor/bin/phpunit
```
