# Replicating the development environment

## Source code repository
https://github.com/wjgibson/limitless-automation-possibilities-visual-IDE

## Tech Aspects
This system is built with react and written in typescript. Through the use of a library called reactflow, nodes are able to be moved around and connected.
These configurations will later be written to a database that communicates with a process entirely seperate from ours.

## Code Replication
### In order to run this app, you will need at minimum the following programs.
NodeJS: https://nodejs.org/en/<br>
Any IDE (If needed, visual studio code is simple and will suffice): https://code.visualstudio.com/

### Steps to replicate using visual studio code
1: Navigate to the main page of the source code repository (link posted above) <br>
2: Click the green drop down box labeled "Code" and copy (`CTRL C`) the link located there<br>
3: Open visual studio code to the welcome screen and select "clone git repository"<br>
4: In the bar that pops up at the top, paste (`CTRL V`) the link previously copied<br>
5: Click "Select repository location" to accept the default folder location<br>
6: Click "Open" on the resulting popup box<br>
7: Enter the following key combination "`CTRL ~`" (Control tilde)<br>
8: Enter the following commands<br>
9: `npm install` This might take a few minutes as our testing suite is quite large, so don't be alarmed. Constant improvements are being made to decrease this loading time<br>
10: `npm start`<br>
11: Your computers local internet browser will open to the app

## Folder Structure
Inside the app's folder, there are three sub-folders and some miscellaneous files. 
- The "cypress" folder contains the files used to test our app.
- The "public" folder contains files created with create-react-app. These act as backup html pages in case the app doesn't load
- The "src" folder contains to subfolders and one file:
  - "app": contains the main react component to be rendered
  - "elements": contains react elements that are implemented in the app's drag and drop flow component
  - "index.js" is used by react to compile the app and load it in the DOM

## Troubleshooting
If app doesn't run correcttly, there are no logs currently set up. Here are the two most common errors we have encountered and their solutions.
### `npm is not recognized as a command or commandlet...` 
- This error comes from not having node installed. Navigate to nodejs's download page and install node according to the instructions provided. If node was recently installed, a computer restart may be required to add the binary to your PATH variables.
### `npm start is not a script or executable...`
- This error results from executing `npm start` before executing `npm install`. Make sure to do an `npm install` first, then try again.

## Running tests
We have used cypress to test the react components of our app. To run the tests, simply execute the command `npx cypress run --component`. This takes a few seconds and results in all of our tests running in the command line. For a detailed run of the tests in a simulated DOM environment, execute `npx cypress open`and select "component testing" to view our testing classes. Select one of the components and see them open in the simulated DOM.


