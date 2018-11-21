Install multisite (subdomains):
===============================
**1) Download WordPress:**
```
wp core download
```

If you need a specific version, use:
```
wp core download --version=<your_specific_version>
```

**2) Create wp-config.php:**
```
wp core config --dbname="your_db_name" --dbuser="your_db_user" --dbpass="your_db_pass" --dbhost="your_db_host" --dbprefix="your_db_prefix"
```

**3) Install multisite:**
```
wp core multisite-install --subdomains --url="example.com" --title="Site Name" --admin_user="username" --admin_password="password" --admin_email="email@example.com"
```

Convert site to multisite:
==========================
**Run this command:**
```
wp core multisite-convert --subdomains
```

After installing multisite:
===========================
**Add the following to your .htaccess file in /path/to/your/site/, replacing other WordPress rules:**
```
RewriteEngine On
RewriteBase <BASE_PATH>
RewriteRule ^index\.php$ - [L]

# add a trailing slash to /wp-admin
RewriteRule ^wp-admin$ wp-admin/ [R=301,L]

RewriteCond %{REQUEST_FILENAME} -f [OR]
RewriteCond %{REQUEST_FILENAME} -d
RewriteRule ^ - [L]
RewriteRule ^(wp-(content|admin|includes).*) $1 [L]
RewriteRule ^(.*\.php)$ $1 [L]
RewriteRule . index.php [L]
```
Change ```<BASE_PATH>``` to your path
Or go to the ```<your_site_url>/wp-admin/network/setup.php``` and copy the second piece of code.

How to uninstall multisite:
===========================
**1) Backup your site**

**2) Edit wp-config.php: **
```
define( 'WP_ALLOW_MULTISITE', true );
define( 'MULTISITE', true );
define( 'SUBDOMAIN_INSTALL', true );
$base = '<BASE_PATH>';
define( 'DOMAIN_CURRENT_SITE', '<DOMAIN_CURRENT_SITE>' );
define( 'PATH_CURRENT_SITE', '<PATH_CURRENT_SITE>' );
define( 'SITE_ID_CURRENT_SITE', 1 );
define( 'BLOG_ID_CURRENT_SITE', 1 );
```

**3) Drop Database Tables: **
1) wp_blogs
2) wp_blog_versions
3) wp_registration_log
4) wp_signups
5) wp_site
6) wp_sitemeta
