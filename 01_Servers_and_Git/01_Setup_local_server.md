When discussing software, a **stack** refers to the technologies a particular application is using. On the web, a stack typically entails an operating system, a web server, a database server, and a particular programming language.

For example, in this course when we deploy our applications on a live server, those servers will be using a &ldquo;LAMP&rdquo; stack:

+ The __L__ stands for __Linux__ - Main operating system the server is using.
+ The __A__ stands for __Apache__ - Open-source web server.
+ The __M__ stands for __MySQL__ - Open-source database server.
+ The __P__ stands for __PHP__ - Web scripting language.

In order to run, debug, and test our applications, we want to mirror this stack on our own local machines, substituting Linux for whatever operating system we use.

We could individually download and install Apache, PHP and MySQL on our computers, but a simpler approach is to use a program that manages all three such as [MAMP](https://mamp.info) or [XAMPP](https://www.apachefriends.org/index.html).

While both MAMP and XAMPP are cross-platform, experience in past semesters suggest that MAMP works best for Mac users and XAMPP works best for PC users, so that is my reccommendation. Below are instructions for setting up both.


## MAMP Setup on Mac
Download and install MAMP: <https://mamp.info/en/downloads>

<small>Note: The download includes both free *MAMP* and *MAMP Pro* (paid version). You'll only need to use the free MAMP version in this class.</small>

In **Preferences > Web Server**, note that the **Document Root** is, by default, set to `/Applications/MAMP/htdocs`.

<img src='http://making-the-internet.s3.amazonaws.com/vc-mamp-htdocs-document-root@2x.png' class='' style='max-width:603px; width:100%' alt=''>

The Document Root is where you'll put all your web files and projects. You may want to create a shortcut to this directory, because you'll be working in it a lot.

Also in Preferences, under **Ports** click *Set Apache & MySQL* ports to `80` & `3306`:

<img src='http://making-the-internet.s3.amazonaws.com/vc-mamp-ports@2x.png' style='width:100%; max-width:540px'>

The default Apache port is 80, so setting it to this makes it so you can access your local sites via the url `http://localhost`. If your Apache port is something else, for example, 8888, you'd have to access your sites via `http://localhost:8888`.

After you adjust your ports, MAMP should restart your local server.

If you see **two little green dots** next to *Apache* and *MySQL Server*, you know everything started okay.

<img src='http://making-the-internet.s3.amazonaws.com/vc-mamp-mac-all-systems-go@2x.png' class='' style='max-width:723px; width:100%' alt=''>

If either of these services don't start up, you'll want to read these notes: [__Debugging your local server__](https://github.com/susanBuck/dwa15-fall2016-notes/blob/master/01_Servers_and_Git/02_Debugging_local_servers.md).


### Your first file

With MAMP installed and your local server running, test out your first PHP script: Create a new file in your code editor and save it as `helloworld.php` in `/Applications/MAMP/htdocs/`.

Paste in [this code](https://gist.github.com/susanBuck/3f133c6d64be0f6f27a9) to your `helloworld.php` file.

Finally, load your `helloworld.php` file in your browser via this URL `http://localhost/helloworld.php`.

<img src='http://making-the-internet.s3.amazonaws.com/vc-hello-world-done-on-mac@2x.png' class='' style='max-width:927px; width:100%' alt=''>

That's it! Your local server for Mac is installed, running, and tested.


## XAMPP Setup on Windows
Download **[xampp-win32-7.1.8-0-VC14-installer.exe](https://www.apachefriends.org/xampp-files/7.1.8/xampp-win32-7.1.8-0-VC14-installer.exe)**.

Install XAMPP...

[Enlarge...](http://making-the-internet.s3.amazonaws.com/vc-xampp-install-on-windows@2x.png)
<img src='http://making-the-internet.s3.amazonaws.com/vc-xampp-install-on-windows@2x.png' class='' style='max-width:1038px; width:100%' alt=''>

Once installation is complete, from the XAMPP Control Panel, start Apache and MySQL.

If all goes well, *Apache* and *MySQL* in the *Modules* column should light up with a green background.

<img src='http://making-the-internet.s3.amazonaws.com/vc-xampp-win-start-servers@2x.png' class='' style='max-width:723px; width:100%' alt=''>

If either of these services don't start up, you'll want to read these notes: [__Debugging your local server__](https://github.com/susanBuck/dwa15-fall2017/blob/master/01_Servers_and_Git/02_Debugging_local_servers.md).


### Your first file
Assuming your local server is now running, test out your first PHP script: Create a new file in your code editor and save it as `helloworld.php` in `c:/xampp/htdocs/`. This path is your local server's **Document Root** which is where you'll put all your web files and projects. You may want to create a shortcut to this directory, because you'll be working in it a lot.

Paste in [this code](https://gist.github.com/susanBuck/3f133c6d64be0f6f27a9) to your `helloworld.php` file.

Load your `helloworld.php` file in your browser via `http://localhost/helloworld.php`.

<img src='http://making-the-internet.s3.amazonaws.com/vc-confirm-localhost-working-xampp-on-win@2x.png' class='' style='max-width:579px; width:100%' alt=''>

That's it! Your local server for Windows is installed, running, and tested.
