A Short Primer on Webpages
==============================

Building Blocks of Webpages
------------------------------

Creating a webpage from scratch (without tools such as React) requires two components: a frontend (visuals that users see + functionality) and a backend (means to process and store user inputs). For the most part, we will be dealing with frontend scripts.

Frontend
------------------------------
What I will call "pure" frontend (often times referred to as the "static" page) is written in HTML (tools such as React generate HTML files that are then displayed). Pure frontend constructs the physical shapes, colors, and text we see on webpages.

If you hit `Ctrl + Shift + I`, you can see the source code for a particular page. Hit the Elements tab and you will be able to see the HTML for a particular page. As you hover over different lines of the HTML file, you'll notice that sections of the page might be highlighted. Those paritcular sections of code correspond to the paritcular sections of webpage.

Much of the HTML file will seem like gibberish, don't worry, it's gibberish to us as well. This is a consequence of most HTML files being machine generated from higher level scripts.

HTML
------------------------------
To be clear, the purpose of this section is not to teach you how to write HTML files, but rather to highlight charactertics of HTML files that we can use to extract information from webpages.

HTML denotes objects on the page using "elements" indicated by angled brackets. For example:

.. code-block:: HTML 

    <div>
        <h1>What hath God wrought?</h1>
        <img src="https://upload.wikimedia.org/wikipedia/commons/c/cd/University_of_Chicago_Coat_of_arms.png">
    </div>

In plain English: "inside of a div element (think of this as a container or organizational unit), we have a header and an image"
