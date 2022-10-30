Installing :code:`npm`
--------------------------------
First, to locally host the server, you need to have `npm` installed. You can do this by first installing the `nvm` package manager with the following command

.. code-block:: console

	curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

Then exiting and reopening your terminal and typing:

.. code-block:: console

	nvm install node

To host the server:
1. :code:`npm install` to install all depedencies
2. :code:`npm start`

Adding a new page
--------------------------------

To add a new page, follow the below steps:
1. Add a path to :code:`src/App.js`. To do this, add the line :code:`<Route path="/[endpoint]" element={<[your page] />} />`.
2. At the top of :code:`src/App.js`, add the line :code:`import [your page] from "./pages/[your page].js"`
3. Create a file in :code:`src/pages` called :code:`[your page].js`.

When in doubt, look at the other routes in :code:`src/App.js` as an example.

Creating the page
---------------------------------

Suppose we are creating a page called "Page", your `src/pages/Page.js` file should a bit like this

.. code-block:: javascript

  const Page () => {
    return (
      //some html
    );
  }
  export default Page

When in doubt, look at :code:`src/pages/Layout.js` as an example.
