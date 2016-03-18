# Wine Cellar Sample Application with Backbone.js and Twitter Bootstrap #

"Backbone Cellar" is a sample CRUD application built with Backbone.js and Twitter Bootstrap. The application allows you to browse through a list of wines, as well as add, update, and delete wines.

This application is further documented [here](http://coenraets.org/blog).

The application is also hosted online. You can test it [here](http://coenraets.org/backbone-cellar/bootstrap).

The application is provided with a RESTful back-end implemented in PHP (see the /api directory).

To use the app with the persistent RESTful back-end, set up the database as documented below and comment out the memorystore.js script import in index.html.

## Database Set Up: ##

1. Create a MySQL database name "cellar".
2. Execute cellar.sql to create and populate the "wine" table:

	mysql cellar -u root < cellar.sql
