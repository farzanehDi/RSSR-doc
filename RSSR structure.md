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
>Every app wants a starting point,in the RSSR project the provider folder is the head of this app.
This folder is the starting place that defining the basic settings needed to run app.

<a id="public">public</a>
>This folder is a place to store everything we want to have directly and raw on the output.
Everything in this folder will be directly accessible.

## src
>This folder is the location of our app definition.
A large percentage of what we expect from the app is defined and maintained in this folder.

## .babelrc
>Used for babel file settings.

## .env
>Files containing environment variables used for various execution modes, including:
-- .env
-- .env.development
-- .env.production
-- .env.test

## eslintrc
>Is a file that contains the es-lint settings. As you know, this is a file that helps us code better.

## basic Requirements
>Includes basic requirements for the app, including:
-- .gitignore
-- package.json
-- readme.md
