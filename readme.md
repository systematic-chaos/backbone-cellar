## Wine Cellar Sample Application
- Code originally from https://github.com/ccoenraets/backbone-cellar

"Backbone Cellar" is a sample application built with [Backbone.js](http://documentcloud.github.com/backbone/).

The application allows you to browse through a list of wines, add, update, and delete wines.

### Changes in this repository with respect to original code
Three versions of the application are available, each one in the corresponding folder:
* bootstrap

  This version uses an in-memory datastore.
  This application is ready to be run as a Docker container in the: [cursocloudaws/backbone-cellar-mem](https://hub.docker.com/r/cursocloudaws/backbone-cellar-mem/) Docker Hub repository.

* bootstrap-sql-docker

  This version has been modified to support the execution in Docker containers via the [Legacy container links](https://docs.docker.com/engine/userguide/networking/default_network/dockerlinks/). In particular, environment variables are read at runtime to automatically discover a MySQL container that hosts the wines database (see ```api/index.php::getConnection()``` for details).
 A MySQL-based back-end is required by a linked MySQL Docker container.

  This application is ready to be run as a Docker container in the [cursocloudaws/backbone-cellar-sql-docker](https://hub.docker.com/r/cursocloudaws/backbone-cellar-sql-docker/) Docker Hub repository.


* bootstrap-sql-docker-compose

  This version has been modified to support the execution in Docker containers using [Docker container networking](https://docs.docker.com/engine/userguide/networking/) (as opposed to the legacy container links). In particular, environment variables are read at runtime to access a MySQL container that hosts the wines database (see ```api/index.php::getConnection()``` for details).

  This application is ready to be run via Docker Compose using the Docker Image available in  [cursocloudaws/backbone-cellar-sql-docker-composed](https://hub.docker.com/r/cursocloudaws/backbone-cellar-sql-docker-compose/) Docker Hub repository.
