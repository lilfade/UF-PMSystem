__Current Status: Working, still needs work - 8/28/14__
__Don't post on the main UF repo asking for support for files not found ow any other error unless it is because of UF and not the plugin__

__Broken as of UserFrosting v0.2.0__

UF-PMSystem
===========
UserFrosting Private Message System, this includes a fully automated installer (almost there!) and is compatible with the current beta version of UserFrosting (0.2.1 at the moment, not master 0.2.0 (no plugin or nav support in 0.2.0 yet)).

Currently everything should work out of the box. You have to install via the script and add the code in the Install section below and it should all work good.

There is a issue with displaying reply's from the db they don't show up in the inbox rather they show in the outbox. This due to how both are coded and this may require a rewrite of the code for that but other then that issue everything should work fine. When installed the pm system is enabled by default if you want to disable it goto your site settings and uncheck the box for the pm system.

Install: visit domain.tld/privatemessages/install/ and follow instructions.

Support requests: If you can't figure something out please open a issue and wait for me or someone to answer you, please reframe from posting on the UF main project as this is not a core plugin and support for anything but the main core should not happen there.


Manual Changes required for install:
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
