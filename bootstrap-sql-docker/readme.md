### Wine Cellar Sample Application with Backbone.js and Twitter Bootstrap #

"Backbone Cellar" is a sample CRUD application built with Backbone.js and Twitter Bootstrap, originally developed by [Christophe Coenraets](http://coenraets.org) and published in the [backbone-cellar](https://github.com/ccoenraets/backbone-cellar) GitHub repository. The application allows you to browse through a list of wines, as well as add, update, and delete wines.
This application is further documented [here](http://coenraets.org/blog).

The application is also hosted online. You can test it [here](http://coenraets.org/backbone-cellar/bootstrap).

The application is provided with a RESTful back-end implemented in PHP (see the /api directory).

Dockerfile and adaptation to run inside a Docker container created by [Germán Moltó](http://www.grycap.upv.es/gmolto) for the [Curso Online de Cloud Computing con Amazon Web Services](http://www.grycap.upv.es/cursocloudaws).


### Prerequisite: MySQL Set Up

1. Download SQL dump for the "cellar" database
```sh
curl -O https://raw.githubusercontent.com/gmolto/backbone-cellar/master/cellar.sql
```

2. Run a MySQL Docker container

```sh
docker run --name mysql -p 3306:3306 -e MYSQL_USER=root -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=cellar -d mysql
```
Change the root password, if required.

3. Populate the "cellar" database
```sh
	mysql -h $DOCKER_HOST_IP -u root -p cellar < cellar.sql
```
This assumes the $DOCKER_HOST_IP variable populated pointing to the Docker Host.
You may omit the -h argument if the Docker engine runs directly on your machine.

### Usage

```sh
docker run -p 80:80 -d --name backbone-cellar-sql-docker --link mysql:mysql backbone-cellar-sql-docker
```
The application will be exposed at port 80 in the Docker Host: http://Docker_Host_IP

You can let Docker decide a free port in the Docker Host:

```sh
docker run -P -d --name backbone-cellar-sql-docker --link mysql:mysql backbone-cellar-sql-docker
```
Use the following command to find out the used port:

```sh
docker port backbone-cellar-sql-docker 80
0.0.0.0:32776
```
The application will be exposed at: http://Docker_Host_IP:32776
