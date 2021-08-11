# XAMPP Development Environment

PHP is a server side language, so we can only see how it runs when we start the local server. For that, we can install [XAMPP](https://www.apachefriends.org/index.html), a web server stack consisting of PHP, MariaDB and Apache Server.

It is available in Windows, Mac and Linux.

<hr>

## Start Up

After launching the app, at the **General** tab, click **Start** to start the XAMPP virtual machine. 

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/xampp1.png?raw=true" style="width:70%" />
  <figcaption></figcaption>
</figure>

Then we can go to the **Service** tab and start the required services.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/xampp2.png?raw=true" style="width:70%" />
  <figcaption></figcaption>
</figure>

We can choose to *mount* the volume, at the **Volume** tab so that we can access and add folders and files inside.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/xampp2.png?raw=true" style="width:70%" />
  <figcaption></figcaption>
</figure>

<hr>

## Enable Remote Access to phpMyAdmin

To access **phpMyAdmin**, a browser admin service for MySQL/MariaDB, at the General tab, click **Go to Application**. This opens a browser where the top right tab goes to it.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/xampp4.png?raw=true" style="width:100%" />
  <figcaption></figcaption>
</figure>

However, on first launch, access to it is blocked by default. 

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/xampp3.png?raw=true" style="width:90%" />
  <figcaption></figcaption>
</figure>

Steps to unblock is shown at the **HOW-TO Guide** tab at the same page. Essentially, we need go into the VM to change some config files. This can be done at the General tab, **Open Terminal**. Within the terminal, install an editor like nano.

!!! note
if you mount the volume, you can directly access the file in your own terminal.

```bash
apt-get update
apt-get install nano
```
<hr>

## Creating a Database

To create a database in MySQL, we click on the tab **Database**.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/myphpadmin1.png?raw=true" style="width:100%" />
  <figcaption></figcaption>
</figure>

Create a database name and click **Create**. The database can be accessed at the left panel.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/myphpadmin2.png?raw=true" style="width:100%" />
  <figcaption></figcaption>
</figure>

If we want to load all the data from another MySQL database, let's say from your production server, we can go to the **Export** tab (make sure you select your database first at the left panel first), and export the tables creation, as well as all the data within each table in SQL.

To load them in your new database in your local server, we can either click on the **Import** tab and load that SQL in; or copy the entire SQL script you exported and go to the **SQL** tab and paste the script in.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/myphpadmin3.png?raw=true" style="width:100%" />
  <figcaption></figcaption>
</figure>


## Launching your Website

After mounting your volume, enter the directory and go into the folder **htdocs**; this is where all your web files are read from in your browser. You can dump your entire folder of website here.

To access it use the **IP Address** indicated at the **General** tab of XAMPP app, together with your folder name you place in the *htdocs* directory, E.g. https://192.168.64.3/uforest. It should load if it has a index.html or index.php inside. There might be some browser security warnings, but you can ignore them since you know that you are loading your own website.

Note that if you have a username and password in your configs for ur website to access MySQL. You will need to change it to the defaults, username as **"root"**, and password as **""**.

## Error Logs

For effective debugging, your php log files are stored in the `/opt/lampp/logs/` folder. For exceptions, you can print out php info `echo phpinfo();` in your website and search for the **error_log** row.

To clean out the logs in the log file, enter into the terminal and `rm error_log`. A new file will be created automatically.

## Upload Files

XAMPP does not allow your code to have permissions to upload file. So if you use `move_uploaded_file()` you will get a Permissed Denied error. You can use the liberal `sudo chmod 777 images/` to the folder to allow access.
