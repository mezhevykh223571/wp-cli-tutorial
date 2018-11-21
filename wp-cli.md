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
```
chmod +x wp-cli.phar
sudo mv wp-cli.phar /usr/local/bin/wp
```

Now try running ```wp --info``` to make sure it is installed.

Updating WP-CLI:
================
```
wp cli update
```
If WP-CLI is owned by root, use:
```
sudo wp cli update
```
