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

Install plugins:
================
**1) Search plugins:**
```bash
wp plugin search <plugin_name>
```
