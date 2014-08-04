UF-PMSystem
===========

Support requests: If you can't figure something out please open a issue and wait for me or someone to answer you, please reframe from posting on the UF main project as this is not a core plugin and support for anything but the main core should not happen there.

Current Status: ___Broken___ - Please dont use unless your pretty good at figuring out a error message and tracing it back to the source. I will update this when my newest changes to UF are commited and thiss will follow to make sure everything works well.

At the moment you need to remove the $template code line from config.php and add
```php
require_once("db-settings.php"); //Require DB connection
require_once("funcs.php");
require_once("password.php"); //<-- add this
```
 see this file for reference: https://github.com/alexweissman/UserFrosting/blob/master/models/config.php
 
=========
=========

UserFrosting Private Message System, this includes a fully automated installer and is compatible with all versions of UserFrosting.

Install: visit domain.tld/privatemessages/install/ and follow instructions.

Temporarily:
Also copy files from the models directory and overwrite default files if default install, if non-default follow the instructions below.

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

2.) find this in models/menu-templates/menu-1.html & menu-2.html:
```html
<ul class="nav navbar-master navbar-nav navbar-right">
	<li class="dropdown user-dropdown">
```	
change to:
```html
<ul class="nav navbar-master navbar-nav navbar-right">
	<li class='navitem-pms'><a href="../privatemessages/pm.php"><i class="fa fa-envelope"></i> Private Messages</a></li>
		<li class="dropdown user-dropdown">
```	
Now run the installer and all should work like it should.
