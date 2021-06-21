# File Transfer Protocol

File Transfer Protocol or FTP, allows you to access and transfer files to and fro your local and web server in production. [FileZila](https://filezilla-project.org) is one of the popular FTP software that is available among Windows, Mac and Linux. Personally for Windows, I usually prefer [WinSCP](https://winscp.net/eng/download.php) for its cleaner interface.

We will need to store the credentials of our web hosting connection at **site manager**, by clicking the top left icon. Click on the **new site** button to create a new site, and enter the **host**, **username** and **password** for your web host.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/ftp2.png?raw=true" style="width:100%" />
  <figcaption>Site Manager</figcaption>
</figure>

The left panel shows the local files and directories in your machine, while the right shows your server files and directories. We just need to drag and drop them from one side to another for file transfers. 

The usual way to do this is that after we develop our changes to our website in the local machine, we will transfer the files from left to right to the server. And when we need to do backups, we can transfer the files back to the left.

<figure>
  <img src="https://github.com/mapattacker/php-web-devlopment/blob/master/images/ftp1.png?raw=true" style="width:100%" />
  <figcaption>Interface of Filezila</figcaption>
</figure>