## Wine Cellar Sample Application
- Code Originally from https://github.com/ccoenraets/backbone-cellar

"Backbone Cellar" is a sample application built with [Backbone.js](http://documentcloud.github.com/backbone/).

The application allows you to browse through a list of wines, add, update, and delete wines.

### Changes in this repository with respect to original code
  The application has been modified to support the execution in Docker containers. In particular, environment variables are read at runtime to automatically discover a MySQL linked container that hosts the wines database (see ```api/index.php::getConnection()``` for details).

 Included Dockerfiles and support code for two versions of the application
   + In-memory datastore (available in the bootstrap folder). This application is ready to be run as a Docker container in the [backbone-cellar-mem](https://hub.docker.com/r/cursocloudaws/backbone-cellar-mem/) Docker Hub repository.
   + MySQL-based back-end to be provided by a linked MySQL Docker container (available in the bootstrap-sql-docker). This application is ready to be run as a Docker container in the [backbone-cellar-sql-docker](https://hub.docker.com/r/cursocloudaws/backbone-cellar-sql-docker/) Docker Hub repository.
