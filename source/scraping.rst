Web Scraping
======================

Basic Idea
----------------------
We can easily retrieve the HTML associated with a specific page by pretending we are trying visit the page (sending a "request" for information). The page responds to the request by sending us what to display (eg the HTML). Once we have the HTML in text form, we can parse out information from tags. 

For example, suppose we wanted to extract the Nobel laureates from the Wikipedia page for Nobel laureates. In HTML, tables are denoted with the `<table>` tag and table rows with `<tr>`. We could now conceivably look through the text and greedily find `<tr>` tags then capture everything until we get to the next `</tr>` tag (closing the element). 

In this manner, we can extract the information from the HTML. Luckily, the Python package BeautifulSoup does this for us, so we don't need to deal with regular expressions or other methods of parsing strings. 

Retrieving HTML Code
----------------------
To make a long story short, when you view something on the internet, your device makes a request to some location on the internet to receive back an HTML file to then display. We can do this using the Python ``requests`` library.

For example, this bit of code retrieves the HTML for the Wikipedia page for the University of Chicago. You can try it out yourself, print out the text, save it to a ".html" file, then open it up in your browser.

.. code-block:: Python

    import requests
    
    r = requests.get("https://en.wikipedia.org/wiki/University_of_Chicago")
    html = r.text

Scraping HTML
----------------------
Now that we have the HTML, we can look for elements in the code, and extract any data we need.

.. code-block:: Python
   
    import requests
    from bs4 import BeautifulSoup

    # retrieve html of page
    r = requests.get("https://en.wikipedia.org/wiki/List_of_Nobel_laureates")
    html = r.text

    # scrape out table elements
    soup = BeautifulSoup(html, 'html.parser') # specifies what kind of code we are looking at  
    table = soup.find("table") # finds the first <table> element       
    rows = table.find_all("tr") # within the first table element, find all the row elements
    rows_data = []
    # Extract row data
    for row in rows:
        row_data = []
        cells = row.find_all("td") 
        for cell in cells:
            row_data.append(cell.get_text())
        rows_data.append(row_data)


For more information and practice, see `this Lab <https://classes.cs.uchicago.edu/archive/2022/winter/12200-1/labs/lab1/index.html>`_ from an old CS department offering.
