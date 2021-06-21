# htaccess

The `.htaccess` file, placed at the root directory of your website, is an Apache configuration file.

# Set Location of 404 file

This is a generic file showing a user that this url does not exist and usually has some guides on how to nagivate the site. We can indicate the 404 file location in htaccess.

```
ErrorDocument 404 /404.php
```

# Rewriting

Rewriting usually accompanies the bulk of the file. We will need to have a command to on the `RewriteEngine` first. Regular expressions are used to parse the conditions. There is usually a condition to check `RewriteCond` before doing the actual rewriting `RewriteRule`.

```
RewriteEngine On

# remove php extension, if not file or uri
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_URI} !(/$|\.)
RewriteRule ^([^\.]+)$ $1.php [NC,L]

# if not using HTTPS, force to use it
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R]
```