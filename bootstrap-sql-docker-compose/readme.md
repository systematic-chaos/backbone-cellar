### Wine Cellar Sample Application with Backbone.js and Twitter Bootstrap #

"Backbone Cellar" is a sample CRUD application built with Backbone.js and Twitter Bootstrap, originally developed by [Christophe Coenraets](http://coenraets.org) and published in the [backbone-cellar](https://github.com/ccoenraets/backbone-cellar) GitHub repository. The application allows you to browse through a list of wines, as well as add, update, and delete wines.
This application is further documented [here](http://coenraets.org/blog).

The application is also hosted online. You can test it [here](http://coenraets.org/backbone-cellar/bootstrap).

The application is provided with a RESTful back-end implemented in PHP (see the /api directory).

Dockerfile and adaptation to run via Docker Compose created by [Germán Moltó](http://www.grycap.upv.es/gmolto) for the [Curso Online de Cloud Computing con Amazon Web Services](http://www.grycap.upv.es/cursocloudaws).


### Environment variables required for the Cellar PHP application

The following environment variables are consulted by the PHP application:
+ MYSQL_HOST (The hostname or IP of the MySQL container)
+ MYSQL_USER (The username to access the MySQL container)
+ MYSQL_PASSWORD (The password to access the MySQL container)
+ MYSQL_DATABASE (The database name that contains the wines information)
+ MYSQL_PORT (The port in which the MySQL container is running)


### Deploy application via Docker Compose

Use the [following Docker Compose file](https://github.com/gmolto/backbone-cellar/blob/master/bootstrap-sql-docker-compose/cellar-docker-compose/docker-compose.yml).

Deploy the application (MySQL and Cellar Application containers) with:
```
docker-compose up -d
```
Connect to http://<doker-host-ip>. The application will be listening in port 80.
