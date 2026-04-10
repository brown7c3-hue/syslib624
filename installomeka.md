# Introduction

I installed Omeka Classic, which is an open source digital tool used to share digital collections. 

## Documentation

To make sure my installed versions of PHP and MySQL met the requirements for the Omeka system, I used `php --version` and `mysql --version` and compared the versions to what was listed on the Omeka Classic User Manual. 

Next, I used the command `php -m` to list the PHP extensions that are installed on my machine, which did list `mysqli` and `exif`. 

I installed ImageMagick, which is used to work with photo files, with the following commands: 

```
sudo apt install imagemagick
sudo a2enmod rewrite
sudo systemctl restart apache2
```

Using the setup for WordPress as an example, I entered this command to create a new user and database in MySQL for the Omeka installation: 

```
create user 'omeka'@'localhost' identified by 'XXXXXXXXX';
create database omeka;
grant all privileges on omeka.* to 'omeka'@'localhost';
show databases;
\q
```

I downloaded the latest Omeka Classic release as a Zip file and extracted it in `/var/www/html` using `wget`. Then, I unzipped the file and named the directory omeka-3.2, so my primary working directory ended up being `/var/www/html/omeka-3.2`. 

I found the `db.ini` file in the extracted directory and added my new database credentials. 

I ran the following command to give Apache group write access on all files and then restarted Apache after this. 

```
cd /var/www/html/omeka-3.2
sudo chmod -R g+w *
```

I completed the Omeka setup via the web form like I did with WordPress. 


# Reflection

Honestly, at some point I got really stuck. I encountered several errors while setting up Omeka, but I was able to receive some guidance in the discussion board for questions. I did make the mistake of not detailing everything I was doing while trying to fix my mistakes because my mind was solely focused on trying everything. At some point, I was able to get Omeka up and running, but I’m not quite sure what I did. I know I should have been documenting my work, but I was only thinking of my actual work and trying to resolve the issue that arose. I referenced the chapter on WordPress often while working on this assignment, and I also had to return to the chapter on Apache as I encountered some errors. 

This was one of the most difficult assignments I’ve completed in this course as I have grown used to following a step-by-step chapter. However, this was also good practice for when I do step into a librarian role. I find myself always seeking guidance, yet I know at some point I need to be able to make decisions on my own and without step-by-step instructions. I appreciate this assignment and how it pushed us to try and apply what we’ve been learning throughout the course. 
