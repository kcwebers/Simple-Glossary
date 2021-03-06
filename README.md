# Glossary of Key Items (Python Related)

## Python General

### decorator

"Decorators are very powerful and useful tool in Python since it allows programmers to modify the behavior of function or class. Decorators allow us to wrap another function in order to extend the behavior of the wrapped function, without permanently modifying it. But before diving deep into decorators let us understand some concepts that will come in handy in learning the decorators."
- https://www.geeksforgeeks.org/decorators-in-python/

### flask

"Flask is a web framework, it’s a Python module that lets you develop web applications easily. It’s has a small and easy-to-extend core: it’s a microframework that doesn’t include an ORM (Object Relational Manager) or such features."
- https://pythonbasics.org/what-is-flask-python/

### framework

"A web framework (WF) or web application framework (WAF) is a software framework that is designed to support the development of web applications including web services, web resources, and web APIs. Web frameworks provide a standard way to build and deploy web applications on the World Wide Web. Web frameworks aim to automate the overhead associated with common activities performed in web development. For example, many web frameworks provide libraries for database access, templating frameworks, and session management, and they often promote code reuse.[1] Although they often target development of dynamic web sites, they are also applicable to static websites.[2]"
- https://en.wikipedia.org/wiki/Web_framework

## Flask (code aspects)

### @app.route("/")

"The "@" decorator associates this route with the function immediately following... We set up a routing rule using the "@" decorator with the route method: @app.route("/route_string"). The routing rule is associated with the function immediately following it."
- https://login.codingdojo.com/m/172/7219/52126

In simpler terms, using ` @app.route() ` "catches" a url and then runs a block of code in association with that route. A complete app route might look like the following, where the route ` '/hello' ` is caught and a function is ran that ultimately returns the HttpResponse of ` Hello World! `
```PY
@app.route('/hello')
def hello_world():
    return 'Hello World!' 
```

### server.py and structure

The ` server.py ` is the main engine of our projects as it is the file we will run! Every ` server.py ` file should have the same components at the top and bottom:

```PY
from flask import Flask # you can add additional imports like render_template here
app = Flask(__name__)

# app routes and functions go in the middle of the server file


if __name__=="__main__":
    app.run(debug=True)
```

The first 2 lines and the final 2 lines work together to make the engine run for our projects. If they are incorrect or out of place, you application may not run properly!

The first line imports Flask and makes it available for us to use.
The second line creates an instance of our imported Flask class and names it ` app `.

The second to last line "Ensure[s] this file is being run directly and not from a different module" by associating our project `__name__` with `__main__`.
The last line is the line that actually runs our established app (from line 2) in debug mode.
- https://login.codingdojo.com/m/172/7219/52126

### linting errors

"...you may see some red squiggly lines under your import statements because your text editor's linter doesn't recognize packages in your virtual environment. You can ignore them unless running the file actually gives you errors!"
- https://login.codingdojo.com/m/172/7219/52126

### Routes

"Routes are an essential part of any web application. A route is much like a variable name we assign to a request. The job of a route is to communicate to the server what kind of information the client needs. This route name is attached to a route on our server that points towards a specific set of instructions. These instructions contain information about how to interpret the data being sent, the operations that need to be completed, and the response that should be sent back. These instructions are the code we'll be creating!
Every route has two parts: HTTP method (GET, POST, PUT, PATCH, DELETE), and a URL"
- https://login.codingdojo.com/m/172/7219/52127

### Root Route

The root route is the base route of a url: ` "/" `

- https://login.codingdojo.com/m/172/7219/52129

### HTTP methods

GET - "GET is used to request data from a specified resource."

POST - "POST is used to send data to a server to create/update a resource."

**Because we will only be using GET and POST in the Python stack, I will only include the definitions for those here**

- https://www.w3schools.com/tags/ref_httpmethods.asp

### render_template() 

This is a function that "...that allows us to return the rendered HTML that we created."
- https://login.codingdojo.com/m/172/7219/52129

### Template Engines

"A template engine enables you to use static template files in your application. At runtime, the template engine replaces variables in a template file with actual values, and transforms the template into an HTML file sent to the client. This approach makes it easier to design an HTML page"

**NOTE:** This definition comes from a discussion about Express (a javascript language) however proved a simple and clear explanation of what a template engine is in general.

- https://expressjs.com/en/guide/using-template-engines.html