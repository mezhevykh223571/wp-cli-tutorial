Install WordPress:
==================
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

**3) Install WordPress:**
```
wp core install --url="example.com" --title="Site Name" --admin_user="username" --admin_password="password" --admin_email="email@example.com"
```

Plugins:
========
**1) Search plugins:**
```
wp plugin search <plugin_name>
```

If you want to see more that 10 plugins on per page:
```
wp plugin search <plugin_name> --per-page=<number>
```

**2) Install plugins:**
```
wp plugin install <plugin_name>
```

**3) Activate plugins:**
```
wp plugin activate <plugin_name>
```

**Installation and activation by one command:**
```
wp plugin install <plugin_name> --activate
```

**4) Update plugins:**
```
wp plugin update <plugin_name>
```

**5) Update all plugins:**
```
wp plugin update --all
```
**6) Show installed plugins:**
```
wp plugin list
```
**7) Uninstall plugins:**
```bash
wp plugin uninstall <plugin_name>
```

Themes:
=======
**1) Search themes:**
```
wp theme search <theme_name>
```

If you want to see more that 10 theme on per page:
```
wp theme search <theme_name> --per-page=<number>
```

**2) Install themes:**
```
wp theme install <theme_name>
```

**3) Activate themes:**
```
wp theme activate <theme_name>
```

**Installation and activation by one command:**
```
wp theme install <theme_name> --activate
```

**4) Update themes:**
```
wp theme update <theme_name>
```

**5) Update all themes:**
```
wp theme update --all
```
**6) Show installed themes:**
```
wp theme list
```
**7) Uninstall themes:**
```
wp theme uninstall <theme_name>
```

Update WordPress core:
======================
```
wp core update
wp core update-db
```
