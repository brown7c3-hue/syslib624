# Introduction

An Online Public Access Catalog (OPAC) is a tool used to search a library’s collection, which is managed by integrated library systems (ILS). An OPAC is created once a LAMP stack is established, as LAMP (Linux, Apache, MySQL, PHP) allow content management systems to function properly. In Module 5, I learned to create a very basic [OPAC] (http://35.188.18.102/mylibrary.html) as well as a [cataloging module] (http://35.188.18.102/cataloging/index.html). 

# Relational Database Structure

Relational databases are important tools as they are able to manage and retrieve data in an efficient manner as data is spread over different tables, which helps limit duplication of data. Data from relational databases are entered through the use of LAMP technologies. MySQL is one example of a relational database. A relational database is also what defines an OPAC or discovery service and separates them from other databases available online as it stores records that have been structured in a certain way. 

# Setup

## Database Connection

To begin creating a basic OPAC, I started by updating my table with the following code: 

`` 
mysql -u opacuser -p
mysql> use opacdb;
mysql> alter table books add publication_date date;
mysql> update books set publication_date = str_to_date(concat(copyright, '-01-01'), '%Y-%m-%d');
mysql> alter table books drop column copyright;
mysql> alter table books change publication_date copyright date not null;
``

Once the table was updated, I created a basic HTML page called mylibrary.html, which included a form for entering queries. A PHP script (search.php) is established after a user clicks submit on the form, and this establishes the connection to the OPAC database I created. 

## Cataloging Module

An ILS is made up of the cataloging module as well as the following modules: acquisitions, authority files, circulation, course reserves, patron management, and more. Once I created my username and password for my cataloging module, I was able to add records. 


I used the commands below to create a new directory and a new index.html file for my cataloging module:

``
cd /var/www/html
sudo mkdir cataloging
cd cataloging
sudo nano index.html
``

## Search and Retrieval

In order to retrieve data from the books table, I had to create a PHP file. I was able to perform the search function as a result of the MySQL query contained in the PHP script. 

## Real-world 

One thing that is necessary to make the OPAC and Cataloging Modules more real-world like would be to use more than one table as ILS typically relies on dozens of tables. A real-world system also has more security measures in place to prevent entering wrong data. 

## Details and Documentation 

In order for the system to function properly, I had to make sure the form matched the data structure in the books table I created previously, which included the following elements: author, title, publisher, and copyright. 

When typing out the different codes for this module, I simply followed the provided materials. I did not look up documentation during this module. 

# Reflection 

I really enjoyed this module. In previous courses, I read about Online Public Access Catalogs (OPAC), but I think I developed a better understanding through the act of creating a basic OPAC myself. Although I work in my library’s Cataloging and Processing department, I do not know as much about cataloging as I do about processing (which is my current area of work). I thought it was fun being able to enter information into my OPAC, even if it was only a few simple elements (author, title, publisher, and copyright). 

All of the chapters and directions were clear and intuitive. I did not perform additional research, and I did not have to troubleshoot anything. I think I had an easier time during my work on this module than I have in previous modules as I made sure to slow down and take my time when entering commands and when reading the chapters. I had very minimal if any mistakes while setting up my OPAC and cataloging module. Throughout previous modules as well as this module, I have learned that it is critical to have a great level of attention to detail while working with databases, software code and system documentation especially given that this work will affect its accessibility for library users. Misspelling and entering incorrect information can negatively affect a user’s experience with retrieving information they may be searching for. 

Even though I only created a really basic OPAC and cataloging module for this assignment, the foundation of the work connects well to real-world library systems and their maintenance. I had to learn several tools before even creating these systems through the LAMP stack, but this helped me understand how everything is connected. It is necessary to understand the foundations of anything before working on a project at a larger scale (such as larger library systems that require the use of dozens of tables in their databases). 
