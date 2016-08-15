# inpsyde-wp-nonce



## Installation
```shell
	composer require asvinb/wp-nonce-oo
```

## How to use

Create nonce
```php
	$nonce = \Inpsyde\Inpsyde::wp_create_nonce();
```

Verify nonce
```php
	$isValid = \Inpsyde\Inpsyde::wp_verify_nonce($nonce);
```

Create nonce hidden input
```php
	\Inpsyde\Inpsyde::wp_nonce_field();
```

Generate nonce URL:
```php
	$url = \Inpsyde\Inpsyde::wp_nonce_url('http://www.google.com');
```

Check if request was been referred from an admin screen:
```php
	$admin = \Inpsyde\Inpsyde::check_admin_referer();
```

Verifies the AJAX request to prevent processing requests external of the blog.
```php
	$ajax = \Inpsyde\Inpsyde::check_ajax_referer();
```

## Testing
```shell
vendor/bin/phpunit
```

Do update the WP_INSTALL constant in phpunit.xml to a local working WordPress installation

## Changelog

### 0.1 
Initial version
