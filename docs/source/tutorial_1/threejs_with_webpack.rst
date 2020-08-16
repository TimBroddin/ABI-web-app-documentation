Tutorial 1 - Building threejs apps with Webpack
===============================================

Overview
--------
This tutorial describes how to setup a threejs web app using Webpack 4. To learn more about Webpack, watch the following `Getting Started Guide <https://www.youtube.com/watch?v=TzdEpgONurw>`__ by Gary Simon.

Setting up a Webpack 4 project
------------------------------

1. Open a terminal and make a project folder.

  .. code-block:: bash
    :linenos:

     mkdir your_project_name
     cd your_project_name

2. Create an empty :file:`package.json` file.

  .. code-block:: bash

     touch package.json

3. Initialise an npm project.

  .. code-block:: bash

     npm init -y

  This will populate the :file:`package.json` file.

4. Edit :file:`package.json` by replacing the scripts field with the following:

  .. code-block:: json-object
    :force:

     "scripts": {
       "build": "webpack",
       "serve": "webpack-dev-server"
     },

5. Install webpack and it's commandline interface.

  .. code-block:: bash

     npm i -D webpack wepack-cli webpack-dev-server

Running javascript files
------------------------
By default, npm generates the :file:`package.json` to run an :file:`index.js` file located in a :file:`src` folder. We can create this file with the following steps:

1. Create a :file:`src` folder.

  .. code-block:: bash

     mkdir src


2. Create an empty :file:`index.js` file in the :file:`src` folder:

  .. code-block:: bash

     cd src
     touch index.js

3. Run serve

Creating an index.html entry point to our app
---------------------------------------------
By default, webpack will only process the  :file:`index.js` script in :file:`src` without creating any html output. In order visualise our app, we need to create an :file:`index.html` file and tell webpack it's location using the following steps:

1. Install the `html-webpack-plugin`.

  .. code-block:: bash

     npm i -D webpack wepack-cli html-webpack-plugin

2. Create a file named `webpack.config.js` with the following contents and place in the root project folder (click this :download:`link <webpack.config.js>` to download a copy of this file).

  .. literalinclude:: webpack.config.js
    :language: javascript
    :linenos:

  This will tell Webpack to serve the :file:`index.html` from the :file:`src` folder.

3. Create a file named `index.html` with the following contents and place in the :file:`src` folder (click this :download:`link <index.html>` to download a copy of this file).

  .. literalinclude:: index.html
    :language: html
    :linenos:

Visualising a rotating cube with threejs
----------------------------------------
1. Replace index.js with the following javascript file.

  .. literalinclude:: index.js
    :language: javascript
    :linenos:

2. Rerun serve









