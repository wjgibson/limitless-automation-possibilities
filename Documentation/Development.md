# Replicating the development environment

## Source code repositories
https://github.com/wjgibson/limitless-automation-possibilities-visual-IDE

https://github.com/wjgibson/lap-visual-ide-API
## Tech Aspects
This system is built with create-react-app and written with javascript. Through the use of a library called reactflow, nodes are able to be moved around and connected.
These configurations will later be written to a database that communicates with a process entirely seperate from ours.

A test database is used due to reconfiguring of their datatabase as the client is changing the type of database they are on, so all the values must be updated to reflect that. Otherwise, LAP would be stuck early on due to that blockage. 

## Code Replication
### In order to run this app, you will need at minimum the following programs.
NodeJS: https://nodejs.org/en/<br>
Any IDE (If needed, visual studio code is simple and will suffice): https://code.visualstudio.com/ <br>
Postgres: https://www.postgresql.org/download/

### Steps to replicate using visual studio code
Repeat most steps for both repositories

1: Navigate to the main page of the source code repository (link posted above) <br>
2: Click the green drop down box labeled "Code" and copy (`CTRL C`) the link located there<br>
3: Open visual studio code to the welcome screen and select "clone git repository"<br>
4: In the bar that pops up at the top, paste (`CTRL V`) the link previously copied<br>
5: Click "Select repository location" to accept the default folder location<br>
6: Click "Open" on the resulting popup box<br>
7: Enter the following key combination "`CTRL ~`" (Control tilde)<br>
8: Enter the following commands for the main repository <br>
9: `npm install` This might take a few minutes as our testing suite is quite large, so don't be alarmed. Constant improvements are being made to decrease this loading time<br>
10: `npm start`<br>
11: Your computers local internet browser will open to the app<br>
12: Enter the following commands for the API repository <br>
13: `npm install` This might take some time.<br>
14: `node API.js` Starts the API running on the port 3001. <br>
15: The project API needs a database in order to run so we need to download postgress<br>
16: Install with default settings <br>
17: While setting up the application make sure that when prompted to create a password you make it `password` <br>
18: Finish setting up postgress and download our mock database dump at https://github.com/wjgibson/lap-visual-ide-API/blob/master/dump-postgres <br>
19: Navigate to the file location in the command line and run this command psql -U -f dump-postgres.sql <br>
20: The database should now be ready to be used by the API <br>

## Folder Structure
Inside the main app's folder, there are three sub-folders and some miscellaneous files. 
- The "cypress" folder contains the files used to test our app.
- The "public" folder contains files created with create-react-app. These act as backup html pages in case the app doesn't load
- The "src" folder contains three subfolders and one file:
  - "app": contains the main react component to be rendered
  - "elements": contains react elements that are implemented in the app's drag and drop flow component
  - "resources": contains logic for custom nodes and helps the API
  - "index.js" is used by react to compile the app and load it in the DOM 

Inside the API's folder, there are three important files. 
- "API.js" is the main file for working with the API doing the GET and POST requests.
- "destructiveQueries.js" is a file that does updating of a configuration like the save/restore shown.
- "queries.js" is a file that grabs the data of configurations to pick from.
 
## Troubleshooting
If app doesn't run correcttly, there are no logs currently set up. Here are the two most common errors we have encountered and their solutions.
### `npm is not recognized as a command or commandlet...` 
- This error comes from not having node installed. Navigate to nodejs's download page and install node according to the instructions provided. If node was recently installed, a computer restart may be required to add the binary to your PATH variables.
### `npm start is not a script or executable...`
- This error results from executing `npm start` before executing `npm install`. Make sure to do an `npm install` first, then try again.
### `Module not found: Error: Can't resolve 'antd'`
- If this is shown on the browser, type into the terminal `npm install antd` as elements use antd to make the project look nicer.
## Running tests
We have used cypress to test the react components of our app. To run the tests, simply execute the command `npx cypress run --component`. This takes a few seconds and results in all of our tests running in the command line. For a detailed run of the tests in a simulated DOM environment, execute `npx cypress open`and select "component testing" to view our testing classes. Select one of the components and see them open in the simulated DOM.

To test the API, type `npm test` into the terminal inside the main repository.

## Replicating via Docker
- Install Docker Desktop to your Operating System
- Clone the source reposititories linked [here](https://github.com/wjgibson/limitless-automation-possibilities/blob/main/Documentation/Development.md#source-code-repository)
- Build the docker image by command line for the main repository with `docker build -t lapide .`
- Run the image by command line with `docker run -d -p 3000:3000 --name node-app lapide`
- In a browser's address bar, type `localhost:3000` to see the result
- Build the docker image by command line for the API repository with `docker build -t lapapi .`
- Run the image by command line with `docker run -d -p 3001:3001 --name node-app2 lapapi`

## Linting
- Use the command `npm install eslint` to enable the use of the next command. 
- Use the command `npx eslint "src/**" "test/**" "cypress.config.js" "cypress/component/**" "cypress/support/**" --fix` in the main repository to lint all files which should automatically format all small issues. This also shows bigger issues that automatically could not be solved.
- Use the command `npx eslint "API.js" "destructiveCalls.js" "non-destructiveCalls.js" "queryFile.js"  --fix` in the API repository to lint all files which should automatically format all small issues. This also shows bigger issues that automatically could not be solved.
