### Wine Cellar Sample Application with Backbone.js and Twitter Bootstrap #

"Backbone Cellar" is a sample CRUD application built with Backbone.js and Twitter Bootstrap, originally developed by [Christophe Coenraets](http://coenraets.org) and published in the [backbone-cellar](https://github.com/ccoenraets/backbone-cellar) GitHub repository. The application allows you to browse through a list of wines, as well as add, update, and delete wines.

This application is further documented [here](http://coenraets.org/blog).

The application is also hosted online. You can test it [here](http://coenraets.org/backbone-cellar/bootstrap).

The application is provided with an in-memory datastore that allows you to experience the app without setting up a back-end. All the changes you make to the data will be lost the next time you access the app or hit Refresh.

Dockerfile created by [Germán Moltó](http://www.grycap.upv.es/gmolto) for the [Curso Online de Cloud Computing con Amazon Web Services](http://www.grycap.upv.es/cursocloudaws).

### Usage

```sh
docker run -d -p 80:80 --name backbone-cellar-mem cursocloudaws/backbone-cellar-mem
```
The application will be exposed at port 80 in the Docker Host: http://Docker_Host_IP

You can let Docker decide a free port in the Docker Host:

```sh
docker run -d -P --name backbone-cellar-mem cursocloudaws/backbone-cellar-mem
```
Use the following command to find out the used port:

```sh
docker port backbone-cellar-mem 80
0.0.0.0:32776
```
The application will be exposed at: http://Docker_Host_IP:32776
