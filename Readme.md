Install WP-CLI:
===============
**1) Download wp-cli.phar:**
```bash
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
```

**2) Check if it works:**
```bash
php wp-cli.phar --info
```

**3) To be able to type just wp, instead of php wp-cli.phar, you need to make the file executable and move it to somewhere in your PATH. For example:**
```bash
chmod +x wp-cli.phar
sudo mv wp-cli.phar /usr/local/bin/wp
```

Now try running ```bash wp --info ```. If WP-CLI is installed successfully, you’ll see output like this:

Updating WP-CLI:
================
```bash
wp cli update
```
If WP-CLI is owned by root, use:
```bash
sudo wp cli update
```

Install WordPress:
==================
**1) Download WordPress:**

```bash
wp core download
```

If you need a specific version, use:
```bash
wp core download --version=<your_specific_version>
```

**2) Create wp-config.php:**
```bash
wp core config --dbname="your_db_name" --dbuser="your_db_user" --dbpass="your_db_pass" --dbhost="your_db_host" --dbprefix="your_db_prefix"
```

**3) Install WordPress:**
```bash
wp core install --url="example.com" --title="Site Name" --admin-user="username" --admin-password="password" --admin-email="email@example.com"
```

Plugins:
========
**1) Search plugins:**
```bash
wp plugin search <plugin_name>
```

If you want to see more that 10 plugins on per page:
```bash
wp plugin search <plugin_name> --per-page=<number>
```

**2) Install plugins:**
```bash
wp plugin install <plugin_name>
```

**3) Activate plugins:**
```bash
wp plugin activate <plugin_name>
```

**Install and activate plugins:**
```bash
wp plugin install <plugin_name> --activate
```

**4) Update plugins:**
```bash
wp plugin update <plugin_name>
```

**5) Update all plugins:**
```bash
wp plugin update --all
```
**6) Show installed plugins:**
```bash
wp plugin list
```
**7) Uninstall plugins:**
```bash
wp plugin uninstall <plugin_name>
```

Themes:
========
**1) Search themes:**
```bash
wp theme search <theme_name>
```

If you want to see more that 10 theme on per page:
```bash
wp theme search <theme_name> --per-page=<number>
```

**2) Install themes:**
```bash
wp theme install <theme_name>
```

**3) Activate themes:**
```bash
wp theme activate <theme_name>
```

**Install and activate themes:**
```bash
wp theme install <theme_name> --activate
```

**4) Update themes:**
```bash
wp theme update <theme_name>
```

**5) Update all themes:**
```bash
wp theme update --all
```
**6) Show installed themes:**
```bash
wp theme list
```
**7) Uninstall themes:**
```bash
wp theme uninstall <theme_name>
```

Update WordPress core:
======================
```bash
wp core update
wp core update-db
```
