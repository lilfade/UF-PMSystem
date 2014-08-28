Current Status: Broken, but being fixed check back later - 8/28/14
===========

UF-PMSystem
===========

Support requests: If you can't figure something out please open a issue and wait for me or someone to answer you, please reframe from posting on the UF main project as this is not a core plugin and support for anything but the main core should not happen there.

===========
UserFrosting Private Message System, this includes a fully automated installer and is compatible with the current beta version of UserFrosting (0.2.1 at the moment, not master 0.2.0).

Install: visit domain.tld/privatemessages/install/ and follow instructions.

Modded UF Install:
==================

1.) find this in models/config.php:
```php
// Include paths for pages to add to site page management
$page_include_paths = array(
	"account",
	"forms"
	// Define more include paths here
);
```
change to:
```php
// Include paths for pages to add to site page management
$page_include_paths = array(
	"account",
	"forms",
	"privatemessages",
	"privatemessages/forms"
	// Define more include paths here
);
```
Now run the installer and all should work like it should.
