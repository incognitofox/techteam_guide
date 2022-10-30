Adding Pages
================================

Creating Endpoints
--------------------------------
Open up :code:`src/App.js`, delete everything that's there, and copy in the below code:

.. code-block:: javascript 

	import logo from './logo.svg';
	import './App.css';
	import { BrowserRouter, Routes, Route } from "react-router-dom";
	import LandingPage from "./pages/LandingPage";

	function App() {
	  return (
		<BrowserRouter>
		  <Routes>
			<Route exact path="/" element={<LandingPage />}>
			</Route>
		  </Routes>
		</BrowserRouter>
	  );
	}

Essentially what this bit of code is doing is it is defining our base endpoint, and telling the program that the source file for our landing page is :code:`LandingPage` (which we are importing from :code:`./pages/LandingPage`. So, if our host is "localhost:3000", we have defined our base path as "localhost:3000/". If we want to define a new endpoint, we would add a route under the base route and specify the endpoint and the source file.

First Page
--------------------------------
Now that we've set up our base route, we need to write some code to display something at that route. For organization purposes, we will put all our code for pages that aren't :code:`App.js` in a seperate folder, :code:`pages` with the :code:`src` folder. Now make the file :code:`LandingPage.js` in the :code:`pages` folder.

.. code-block:: javascript

  const LandingPage () => {
    return (
        <div>What hath God wrought?</div>
    );
  }
  export default LandingPage


Adding a New Page
--------------------------------

To add a new page, follow the below steps:

#. Add a path to :code:`src/App.js`. To do this, add the line 

   .. code-block:: html

      <Route path="/[endpoint]" element={<[your page] />} />

   between the :code:`<Route exact ...>` and :code:`</Route>` lines.

#. At the top of :code:`src/App.js`, add the line 

   .. code-block:: python
   
      import [your page] from "./pages/[your page].js"`

#. Create a file in :code:`src/pages` called :code:`[your page].js`.

Upon restarting the server, this new page will be located at :code:`[hostname]/[endpoint]` (eg localhost:3000/test).

Creating the Page
---------------------------------

Suppose we are creating a page called "Page", your :code:`src/pages/Page.js` file should a bit like this

.. code-block:: javascript

  const Page () => {
    return (
      //some html
    );
  }
  export default Page
