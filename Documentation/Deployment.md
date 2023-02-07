# Deploying the LAP Visual IDE

## Server
- Our app runs currently on windows localhost, but does require node and react to run. Installation instructions can be found in our development file.
  - https://github.com/wjgibson/limitless-automation-possibilities/blob/main/Documentation/Development.md

## Download
- The project's source code can be found here
  - Visual IDE: https://github.com/wjgibson/limitless-automation-possibilities-visual-IDE/tree/1.0.0
  - API: https://github.com/wjgibson/lap-visual-ide-API
- Upon donwloading the zip files, unzip each to a location of your preference.

## Start/Stop

### Setting up postgress database

- The project API needs a database in order to run so we need to download postgress
  - https://www.postgresql.org/download/
- Install with default settings
- While setting up the application make sure that when prompted to create a password you make it `password`
- Finish setting up postgress and download our mock database dump
  - Database Dump: https://github.com/wjgibson/lap-visual-ide-API/blob/master/dump-postgres
- Navigate to the file location in the command line and run this command `psql -U -f dump-postgres.sql`
- The database should now be ready to be used by the API

### Starting the API

- Navigate to the location you unzipped the source code to in the file explorer.
- Right click anywhere in the unzipped folder and select `open in terminal`.
- execute the command `npm install`
- execute the command `node API .js`.
- The API should be running.
- Note: this step should be done prior to starting the application or it will not properly work

### Starting the web app

- Navigate to the location you unzipped the source code to in the file explorer.
- Right click anywhere in the unzipped folder and select `open in terminal`.
- execute the command `npm install` (this might take a few minutes).
- execute the command `npm start`.
- App will automatically open up in your default web browser.
- To close the app, simply close the localhost tab.

## Troubleshooting
If app doesn't run correcttly, there are no logs currently set up. Here are the two most common errors we have encountered and their solutions.
### `npm is not recognized as a command or commandlet...`.
- This error comes from not having node installed. Navigate to nodejs's download page and install node according to the instructions provided. If node was recently installed, a computer restart may be required to add the binary to your PATH variables.
### `npm start is not a script or executable...`.
- This error results from executing `npm start` before executing `npm install`. Make sure to do an `npm install` first, then try again.
### `Uncaught TypeError: Can not read properties of undefined...`.
- This error would show up in the developer tools of your console after you try to start the application
### `Error 400: Bad Request`
- This error would show up in the developer tools of yout browser after you try to start the application
- To fix, verify that you setup the postgres server with the password: `password`. If not, the files `queries.js` and `destructiveQueries.js` contain the login info for the database, so change them there.

## Errors
- There is no error logging in the current build of the LAP Visual IDE, but errors can be found in the developer tools console.
- This can be accessed in most browsers with the shortcut `CTRL+SHIFT+I`.

## Potential Disasters
- The most error prone step in this installation is the command execution when running the app. `npm install` must always be ran before `npm start` or the app will fail to compile.
- Within the source code, the most critical file is `MainPage.js`. This contains the main app's code that loads in the browser. If making changes to this file, constantly make sure that the app will still compile.
- The program hinges on having a lot of services running while using it because it is made for web use. If the progam is not running as expected the first place to look would be the API
