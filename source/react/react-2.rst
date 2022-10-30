Using JavaScript
===================================

React lets you write JavaScript and integrate it with HTML.

Above the :code:`return` statement, we can write JavaScript. Within the HTML code you are returning, you can also write JavaScript enclosed in curly braces (:code:`{}`).

For example, try adding the page "Test", and in the source file copy the lines

.. code-block:: javascript

    const Test = () => {
        var myName = "William";
        var myNumMinusOne = 10 - 1;
        return (
            <p>{myName}</p>
            <p>{myNumMinusOne + 1}</p>
        );
    }

React Hooks
----------------------------------
