Deploying the Angular FrontEnd
==============================

Overview
--------
* This repository contains the zoe angular frontend for [zoe](https://github.com/DistributedSystemsGroup/zoe) main repository.

Prerequisites
--------
* Node >= 6.9.0
* NPM >= 3
* [Angular-Cli](https://github.com/angular/angular-cli)

Installation
------------
1. Install Angular-Cli

Please refer to the official [repository](https://github.com/angular/angular-cli).

 * Note: In linux systems it may require root access rights.

2. Install dependencies

From the root directory of the project, run ``npm install``.


Running the server
------------
The server can be started in two different ways.

1. Development Server

 * The first way to install the frontend is to install a local development server; this server will automatically reload when source files are changed. This can be done by the following two steps:

   * Run ``ng serve``
   * Navigate to ``http://localhost:4200/``

2. Proxy Server

 * The second way to install zoe can be done using a proxy with zoe:
 * Run ``ng build -prod --output-path=prod``

   * This will create all the build files in the ``/prod`` directory. These files need to be copied to the frontend server setup in the proxy configuration.
   * Note that in order to change the ``<base href="/">`` within the ``index.html`` file, it is possible to add the following to the ``ng build`` command: ``--base-href x`` where x is the new href value.
 * The output can be put behind a Nginx or Apache proxy.

Read more
---------
More information for deploying the angular project can be found in its documentation at ``DETAILS.md``.
