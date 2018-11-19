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
wp plugin search <plugin_name> --per-page=number
```

**2) Install plugins:**
```bash
wp plugin install <plugin_name>
```

**3) Activate plugins:**
```bash
wp plugin activate <plugin_name>
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


