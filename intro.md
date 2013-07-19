## Introduction Index

1. (Too easy) Introduction
2. Full Stack Composition Description

## (Too easy) Introduction 

We are sure you know about this already, but lets do it again just for giving a structure to the tutorial

In a full stack web application what happens is the following:

Assume the user is sitted in front of the computer. 

The user interface that is presented has the nice things that we see (images and generated things by html and css)

But the user's computer sees code (html, css) that is interpreted to show those nice graphics.

But if the application is interactive, there is some script (javascript) code that actually makes that page change nicely and at a speed that the user does not get annoyed and goes away.

But all this data is represented in a ressource model
So we have an [MVC](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) or [MVVC](http://en.wikipedia.org/wiki/Model_View_ViewModel) [pattern](http://en.wikipedia.org/wiki/Software_design_pattern "design patterns" ) on the client.

And we can go on and say:

But that data came from somewhere (the server), and every time the user writes a post it is sent to the server.
So there must be a communication between server and client. 
There are:
    - [AJAX (protocol)](http://en.wikipedia.org/wiki/Ajax_(programming) "AJAX")
    - [REST (architecture)](http://www.infoq.com/articles/rest-introduction "A nice article introducing REST architecture")

And so the server defines an API for REST that the client can access.

And this data has to be validated, and processed

And stored and given back, 

And the user has to be given only information he can use (and is allowed to see)

Well, there are too many things. 
But we will tacke each of this points


## Full Stack Composition Description

Let's see a simplistic (not fully accurate) version of what the whole stack has:

![General Schema of a full stack modern web app](/imgs/general_schema.png "General Schema of a full stack modern web app")


When a user enters the page what happens is:

1. A message goes to the server asking for the page
2. The server looks for the correct controller and calls it
3. The controller might do the following (it is up to the developer to write down what to do)
    + Validates the request,
    + Check if the user can see the page
    + Asks the DB the data
    + checks tha
4. The controller formats the output data with the template from the views
5. the response is sent to the user's computer and to the web browser
6. The browser puts everything pretty for the user to see
7. Some script might be running now in the web browser waiting for the user to do something
8. If the user does something and the JS script has to process a REST or AJAX call might be done and the process starts all over

### Some extra things on the Server Side:

- Data is stored (in this case) in the devs hard drive, the DB server will be SQlite3

- Web2py will be used as a server side MVC Framework
- Web2py has a web server (rocket)  included for development. 

### Some extra things on the Client side:

- The static visualization is done by your browser
- The dynamic changes to the screen are achieved thanks to some Javascript running in the JS interpreter in the browser



