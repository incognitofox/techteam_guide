Getting started
================================

Installing :code:`npm`
--------------------------------
First, to locally host the server, you need to have `npm` installed. You can do this by first installing the `nvm` package manager with the following command:

.. code-block:: console

	curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

Then exiting and reopening your terminal and typing:

.. code-block:: console

	nvm install node


Creating a New Project
--------------------------------
We will use the package :code:`create-react-app` to build our basic project framework.

.. code-block:: console

    npx create-react-app my-app
    cd my-app
    npm start

This will create a file tree that looks something like this:

.. code-block:: console

	.
	├── README.md
	├── node_modules
	├── package-lock.json
	├── package.json
	├── public
	└── src

The :code:`public` folder contains any data you want to include on your site (think images, data files, etc). The :code:`src` folder contains all the scripts we will use to generate our page.

Within the :code:`src` folder, there is a file :code:`App.js`. This our "main" page, or the script that is run with the command :code:`npm start`.

To host the server:

#. :code:`npm install` to install all depedencies (these are listed in :code:`package.json`) 
#. :code:`npm start`

For more information, see `Creating a New React App <https://reactjs.org/docs/create-a-new-react-app.html>`_.
