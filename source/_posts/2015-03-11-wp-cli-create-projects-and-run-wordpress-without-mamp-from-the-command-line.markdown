---
layout: post
title: "WP-CLI : Create projects and run wordpress without MAMP from the command line."
date: 2015-03-11 00:18:57 -0500
comments: true
categories: ["development", "tools", "php", "wordpress", "cli"]
---


## WP-CLI : the missing command line tool for wordpress
---

## Background

WP-CLI is an amazing suite of tooling that I am embarassed to have only recently found. One of the strangest things as I transitioned to rails from php back in 2011 was the CLI. 

Previously I spent very little time in the command line. My development workflow consisted of switching GUIs. GUIs for almost everything: SourceTree, Coda, MAMP, Eclipse to name a few.

Rails brought everything to the shell. 

`rails new`

`rake db:migrate`

`rails g migration`

While awkward at first I quickly fell in love and my efficiency increased by having a centralized hub for controlling all of the things. The command line.

WP-CLI brings that quick and scriptable interface to php and wordpress.

Installation instructions can be found at: http://wp-cli.org/#install

## Create your first WP-CLI project

To start a new project

`mkdir project_name`

`cd project_name`

`wp core download`

these 3 commands will create a project folder, move into the new folder and then download and extract the latest wordpress release.

## Configure Wordpress

WP-CLI is able to automatically generate a wp-config.php, the easiest way to do this is:

`wp core config --dbname my_project --dbuser webuser --dbpass w3bp@ss`

This command will create a wp-config.php with a database named __my_project__ accessed by a database user named __webuser__ with a password of __w3bp@ss__

## Create a database

WP-CLI has a number of tools for environment management.

`wp db` allows you to interact and perform tasks related to the database.

To create a new database based on your settings in wp-config.php simply type

`wp db create`

## Finalizing Wordpress installation

Finally we must initialize / install wordpress. This basically consists of setting all the configuration related to your wordpress site.

`wp core install --url="www.testing.dev" --title="New site" --admin_user="admin" --admin_password=test --admin_email=justin@kohactive.com`

This command will configure the wordpress installation to live on the domain __www.testing.dev__ with a site title __New site__ and admin user named __admin__ a password of __test__ and an admin email of __justin@kohactive.com__

## Plugin / Theme installation

A super useful feature of WP-CLI is the ability to download and install wordpress plugins and themes from the command line. It is often slow and cumbersome to install these through the web interface and if you have a stack you use time after time it is fairly trivial to automate / script the installation.

`wp theme install https://downloads.wordpress.org/theme/zerif-lite.1.4.7.zip --activate`

This command will download and install the _zerif-lite_ theme, and also activate it.

Common wordpress themes and plugins can also be installed by name.

`wp plugin install woocommerce`

This command will install woocommerce, without specifying a full url to the plug-in.

## Development Server

One of my most sought after features isn't part of wp-cli out of the box. If you are running OSX Yosemite+ however or are handy enough with brew to install a modern php, in my case 5.5.14, you will find that you can run a php development server from the command line.

WP-CLI takes it a step further, and makes it possible to start and serve a wordpress site with a simple command.

`wp server` however you must follow the additional steps on the project repo.

Find the instructions at https://github.com/wp-cli/server-command

Best of luck, find us in #wordpress on the officialy struct.tv slack. Grab a free invite to slack at http://struct.tv
