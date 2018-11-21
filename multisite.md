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
**Add this code to .htaccess:**
```
RewriteEngine On
RewriteBase /
RewriteRule ^index\.php$ - [L]

# add a trailing slash to /wp-admin
RewriteRule ^wp-admin$ wp-admin/ [R=301,L]

RewriteCond %{REQUEST_FILENAME} -f [OR]
RewriteCond %{REQUEST_FILENAME} -d
RewriteRule ^ - [L]
RewriteRule ^(wp-(content|admin|includes).*) $1 [L]
RewriteRule ^(.*\.php)$ wp/$1 [L]
RewriteRule . index.php [L]
```
