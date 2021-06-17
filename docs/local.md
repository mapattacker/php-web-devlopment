# Development Environment

PHP is a server side language, so we can only see how it runs when we start the local server. For that, we can install [XAMPP](https://www.apachefriends.org/index.html), a web server stack consisting of PHP, MariaDB and Apache Server.

It is available in Windows, Mac and Linux.

## Start Up

After launching the app, at the **General** tab, click *Start* to start the XAMPP virtual machine. 

<figure>
  <img src="https://raw.githubusercontent.com/mapattacker/php-web-development/master/images/xampp1.png" style="width:90%" />
  <figcaption></figcaption>
</figure>

Then we can go to the **Service** tab and start the required services.

<figure>
  <img src="https://raw.githubusercontent.com/mapattacker/php-web-development/master/images/xampp2.png" style="width:90%" />
  <figcaption></figcaption>
</figure>

## Enable Remote Access to phpMyAdmin

To access **phpMyAdmin**, a browser admin service for MySQL/MariaDB, at the General tab, click **Go to Application**. This opens a browser where the top right tab goes to it.

<figure>
  <img src="https://raw.githubusercontent.com/mapattacker/php-web-development/master/images/xampp4.png" style="width:90%" />
  <figcaption></figcaption>
</figure>

However, on first launch, access to it is blocked by default. 

<figure>
  <img src="https://raw.githubusercontent.com/mapattacker/php-web-development/master/images/xampp3.png" style="width:90%" />
  <figcaption></figcaption>
</figure>

Steps to unblock is shown at the **HOW-TO Guide** tab at the same page. Essentially, we need go into the VM to change some config files. This can be done at the General tab, **Open Terminal**. Within the terminal, install an editor like nano.

```bash
apt-get update
apt-get install nano
```

