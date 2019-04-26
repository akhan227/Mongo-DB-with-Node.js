# Mongo DB Integration with Node.js

Github Repository Link: https://github.com/akhan227/Mongo-DB-with-Node.js

When it comes to database systems, there are two main types to choose from:
relational or non-relational databases. Another term heavily used is SQL and No-SQL,
since most relational databases are interactd with through the use of SQL.

Relational databases are tabular, flat, and very inflexible. 
Non-relational databases, on the other hand, are not tabular, can be nested, and are very flexible.

Mongo DB is one of the most popular non-relational database systems used in industry
for the advantages non-relational databases bring, but also because the data is stored in a structure
called BSON, which stands for Binary JavaScript Object Notation. The data is already stored in a
JavaScript Object Notation, like JSON, and is easily understandable by most developers without
too much difficulty. 

This project will explain how to use Mongo DB, but also how to integrate it within a web application
using Node.js in order to demonstrante the power of Mongo DB, and also the almost seamless integration
with JavaScript frameworks like Node.js.

## REST
This web application adheres to RESTful routing.
REST stands for Representational State Transfer, which is an architectural style where
data and functionality are considered resources and are accessed using Uniform Resource 
Identifiers (URIs). These resources are acted upon through a set of defined operations. 
They are designed to be a stateless communication protocol using HTTP.

There are multiple RESTful commands, but the most common four are the CRUD method:
* POST:   Create 
* GET:    Read
* PUT:    Update
* DELETE: Delete 

RESTFUL ROUTES Implementation 
    
| NAME     | URL                  | VERB    | DESCRIPTION                                             |
| -------- |:--------------------:|:-------:|--------------------------------------------------------:|
| INDEX    | /employees           | GET     | display a list of all employees                         |
| NEW      | /employees/new       | GET     | displays the form to add a new employee                 |
| CREATE   | /employees           | POST    | adds a new employee to the database                     |
| EDIT     | /employees/:id/edit  | GET     | shows the edit form for one employee                    |
| UPDATE   | /employees/:id       | PUT     | updates a particular employee, then redirects somewhere |
| DESTROY  | /employees/:id       | DELETE  | deletes a particular employee, then redirects somehwere |

## Prerequisites
* NPM and Node.js installed
* Mongo DB installed (Instructions uses Homebrew for Mac OS installation)
* Moderate knowledge of SQL, HTML, JavaScript, Node.js

## Install and Run Mongo DB
This demo was created using the Mac OS X 10.14.4 operating system.
If using any other operating system to run this project, instructions may differ.
Please refer to your OS's documentation to download and configure the software needed for this project.

* Update homebrew
    * `brew update`
* Install Mongo DB to machine
    * `brew install mongodb`
* Create directory where the Mongo data files will be stored
    * `sudo mkdir -p /data/db`
* update permissions for the directory
    * sudo chown -R `id -un` /data/db
* Start the Mongo daemon server
    * `mongod`
* Start the Mongo shell client in another terminal window
    * `mongo`

## Interaction with Mongo DB data
Interacting with the Mongo DB database via the terminal is very similar to
interacting with SQL via the terminal.

Here's how one would go about navigating the terminal via SQL commands:
![SQL Example](https://github.com/akhan227/SQL-vs-NoSQL/blob/master/imgs/sqlExample.png "SQL Example")

Here's how one would go about navigating the terminal via Mongo commands:
![Mongo Example](https://github.com/akhan227/SQL-vs-NoSQL/blob/master/imgs/mongoExample.png "Mongo Example")

After understanding how we created and interact with our Mongo database in this project, you can also see a quick small example on how to create the same database used in SQL [here](https://github.com/akhan227/SQL-vs-NoSQL/blob/master/example.sql).

## Create the Node.js Project
* Create project folder
    * `mkdir MyNodeProject`
* Initialize the npm package.json file
    * `npm init`
* Install npm packages needed for the project
    * `npm install <LIST PACKAGES HERE> --save`
    * Packages used
        * Express: framework that provides a robust set of features for web applications
        * Mongoose: schema-based solution to model application data
        * Body-Parser: HTML form body parsing middleware
        * Method-Override: Lets you use HTTP verbs such as PUT or DELETE since HTML forms do not support it
        * EJS: Embedded JavaScript templates
* Add all of the contents from [this](https://github.com/akhan227/SQL-vs-NoSQL/tree/master/nosql) folder that isn't already present to the directory 
* Start the Mongo daemon server
    * `mongod`
* Run the web app
    * `node index.js`
* Pay close attention to the console that will output the link to access the application, and other important information while using the application
