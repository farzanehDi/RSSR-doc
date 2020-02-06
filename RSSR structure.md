
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
finally the response is passed to the browser.
![](http://webdesignworld.ir/RSSR/RSSR-request.png)
# Folder provider entities
There are three main directories in the provider directory:

 - **server**: Includes node js web server startup files in both development and production modes
 - **setup**: Contains the methods and operations of the privider section, in fact we put here the initial setup we need for the provider discussion
 - **webpack**: this folder contains web pack settings.
 # What happens in the Provider folder
 We have three main command categories:
 
 - The first category is the ***npm run dev*** that run the project to the development mode.
 - The second category is the project execution instructions in production mode.
	 * ***npm run start***:runs the project with node.js
	 * ***npm run start-pm2***:runs the project with pm2
	 * ***npm run up***:In fact, to help with the second command, we use this command to update the project when the project is running with pm-2.
	 
 - The last command is the ***npm run build***, which when we want to execute the production mode, we first execute this command to really build the project and place it on disk and execute the production mode commands.
 
npm scripts execute that file if they hit a file,the ***npm run dev*** command will execute the **development** file located in the server folder and in the provider folder.
If you go inside the development.js file in the server directory you can see that we wrote a node.js web server with express.finally, what appears to be a node.js web server configured to run our project in development mode.

The production commands also execute the production.js file inside the server directory and do the same thing as the development file this time in the production mode, though some configs are different.
***npm run build*** is the command that web pack executes for our project, in fact it processes the src folder to be executed at the end with a set of files specified by us in the web pack configuration.
So far we have three categories of commands that each run one of our three files. The first two commands create a web server that is persistent and survives, but the last command build the project and the job is done.
The other folder we had was the ***setup***, which are methods and operations that can be called in all of them.
The ***development.js*** file in the web pack directory is not executed directly by any command and is for development mode and executes indirectly and build the project files (src folder) except the files are not on disk and in they are RAM because this build is done regularly.
In fact, the result of the npm run build command executes the production.js file in the web pack and ultimately creates a folder called dist at the root of the project, which is a series of physical files.

Both production setting and development setting on the web pack ,call src folder. Connecting the provider section to the src section is done via web pack settings because the src directory is not directly implemented on the node server but is to be compiled on it.

The ***dist*** folder (which is physically) is for production mode and the dist files are directly called in the production.js file.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzExNTQ3MTc0LDg2NDkwOTg1NCwtMjUyNz
gzNDY3LC0xMTY0MDkxODIwLDIzNTI4ODUwOSwtMTg2Mjg4ODc4
NCw4OTAzNTI2ODUsMTQ2NTc5NjQ5MiwtMjQ5ODA1ODA2LDQ4Mj
UzNDMxNiwtMTEzODM4NjAwMywtMTUzMTE5MjIyOSwzNTkyNjYz
MDgsMTYyMDMyODk3Miw3MTYwMjYxNjEsLTE5NTk0MTU1MzUsLT
E5NTI4MTAwNjIsMjAxMzYxMjMyNiwtNDQ0NTM0Nzk1LC0xODEx
OTkyNjU2XX0=
-->