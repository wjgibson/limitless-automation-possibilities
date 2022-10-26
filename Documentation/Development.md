# Replicating the development environment

## Source code repository
https://github.com/wjgibson/limitless-automation-possibilities-visual-IDE

## Tech Aspects
This system is built with react and written in typescript. Through the use of a library called reactflow, nodes are able to be moved around and connected.
These configurations will later be written to a database that communicates with a process entirely seperate from ours.

## Code Replication
### In order to run this app, you will need at minimum the following programs.
NodeJS: https://nodejs.org/en/
Any IDE (If needed, visual studio code is simple and will suffice): https://code.visualstudio.com/

### Steps to replicate using visual studio code
1: Navigate to the main page of the source code repository (link posted above) <br>
2: Click the green drop down box labeled "Code" and copy (CTRL C) the link located there<br>
3: Open visual studio code to the welcome screen and select "clone git repository"<br>
4: In the bar that pops up at the top, paste (CTRL V) the link previously copied<br>
5: Click "Select repository location" to accept the default folder location<br>
6: Click "Open" on the resulting popup box<br>
7: Enter the following key combination "CTRL ~" (Control tilde)<br>
8: Enter the following commands<br>
9: "npm install"<br>
10: "npm start"<br>
11: Your computers local internet browser will open to the app

## Folder Structure
Inside the app's folder, there are two sub-folders and some miscellaneous files. The "public" folder contains common assets used for the project and miscellaneous files created with the app
The "src" folder contains the typescript source code required to run the app. The remaining files are used by node to download the dependencies for the app. There are no
config files that the user must alter at this time.

## Running tests
Running our apps test is simple. In the same console used to replicate the environment in visual studio code, simply type the following command: "npm test". This
has to be done after an "npm install", explained in the steps prior. The console will prompt to select which tests to run, simply enter "a". 
The results in the console will show you how many tests passed and how many faled as well as their names and reasons for failure if applicable.


