
# RSSR structure
The RSSR file has the following structure:
* provider
* public
* src
* .babelrc
* .env
* eslintrc
* basic Requirements

## provider
Every app wants a starting point,in the RSSR project the provider folder is the head of this app.
This folder is the starting place that defining the basic settings needed to run app.

## public
This folder is a place to store everything we want to have directly and raw on the output.
Everything in this folder will be directly accessible.

## src
This folder is the location of our app definition.
A large percentage of what we expect from the app is defined and maintained in this folder.

## .babelrc
Used for babel file settings.

## .env
Files containing environment variables used for various execution modes, including:
-- .env
-- .env.development
-- .env.production
-- .env.test

## eslintrc
Is a file that contains the es-lint settings. As you know, this is a file that helps us code better.

## basic Requirements
Includes basic requirements for the app, including:

-- .gitignore

-- package.json


# How is a request handled by a web application written with RSSR?
Our site is hosted on a server, the browser calls an address that is our site address. This address reaches the Internet and is delivered to our server.
The web server runs a proxy to our RSSR application and this request reaches our application.
Our application, for example, starts with the npm run start command and, for example, is running on port 3000 server , the request that comes will be delivered to that port and entered into our app.
As mentioned earlier, the top of this application is the provider folder,from this folder and the executable tools it is decided which response folder to export (/public or /src)
If it is static and in the public folder it will definitely be delivered to this folder and otherwise to the src folder.
Finally the response is passed to the browser.
![](http://webdesignworld.ir/RSSR/RSSR-request.png)
# Folder provider entities
There are three main directories in the provider directory:

 - server
 - setup
 - webpack

## server
Includes node js web server startup files in both development and production modes
## setup
Contains the methods and operations of the privider section, in fact we put here the initial setup we need for the provider discussion
## webpack
This folder contains web pack settings.


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NTI4MTAwNjIsMjAxMzYxMjMyNiwtND
Q0NTM0Nzk1LC0xODExOTkyNjU2LDIxMTk1NDgzNSwxMjY1NTk2
ODk0XX0=
-->