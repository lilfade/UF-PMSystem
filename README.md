UF-PMSystem
===========

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
