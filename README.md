# DAMP

A Docker application for Apache, PHP, Mysql and PhpMyadmin.

This docker compose application allows you to easily switch the php version as well as rather easily install additional php modules for your application.

ATTENTION: For development purposes only, don't use this on a production server. 

# How it works

clone and cd into this directory, then:
docker compose up
and point your browser to http://localhost:8000

# Configuring your site with mysql

Take notice that in order to connect the mysql database to your website, the mysql host is "mysql" and not "localhost". For example, the configuration.php of a Joomla! installation the reference to the mysql host should be as follows:

    public $host = "mysql";

# initial database

If you uncomment the line:
./mysql/maindb.sql:/docker-entrypoint-initdb.d/maindb.sql
you can initialize the database by placing an sql file called "maindb.sql" in the subdirectory "mysql". 

For example, export your Joomla! database to mysql, then, copy all the Joomla! php files to the html directory and place the sql you just exported as described. Start up the docker and have your database initialized with the sql file.

# Collaboration

Fork this repo, add your functionality and send me a pull request.

