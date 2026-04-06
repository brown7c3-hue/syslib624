# Introduction

For this week’s assignment, I learned about WordPress, and I installed it on my virtual machine. My site is called “Caffeine County Library (Test Site),” which I named after an imaginary library I created for a collection development assignment I completed in another course. 

## Documentation

The first step I completed was making sure all requirements were met in terms of PHP (8.3 or greater) and MySQL (8.0 or greater) versions. 

Next, I downloaded and extracted the WordPress software using the following commands: 

```
cd /var/www/html
sudo wget https://wordpress.org/latest.zip
sudo unzip latest.zip
```

I ran into the issue of not being able to use the “unzip” command, but after watching the video for the assignment I was able to get that fixed. 

I created a new database and user for WordPress after using these commands: 

```
create user 'wordpress'@'localhost' identified by 'XXXXXXXXX';
create database wordpress;
grant all privileges on wordpress.* to 'wordpress'@'localhost';
show databases;
\q
```

I finished the installation process in Google Chrome, where I created my site title, username, and password. I did try to change the theme of my website, but I received an error message when I tried to install a new theme. Specifically, it said, “Installation failed: Could not create directory. /var/www/html/wordpress/wp-content/upgrade.” I wasn’t sure what to do when I saw this message, so I did not end up updating the theme. 

# Summary 
My actual experience with setting up WordPress was pretty smooth. I encountered an error before starting my work on this assignment as I was struggling with connecting to my VM. I was recommended to switch to the e2-small machine type instead of e2-micro for better performance and because it said my machine was over-utilized. I ended up making the switch and tried reconnecting to my VM, and that worked! 

I remember setting up a WordPress website a while ago either in high school or my undergraduate program, but this was quite a bit of a different experience as I had to enter commands through my virtual machine. I think this was a really cool experience as I get the opportunity to see how a website is built from a very general site to a functional and more aesthetic site. 
