<h1>Architecture</h1>
This project will be a monolithic architecture as the project will be JS Frameworks with a database as well. It is a layered type of architecture since neighboring layers matter but the frontend can't talk to the database for example. 
<h2>Drawing</h2>
<img width="1616" alt="Architecture" src="https://user-images.githubusercontent.com/38050891/195405169-14cc289c-cb31-46f8-bf29-049eab3638ed.png">
<h3>MS SQL Database</h3>
Contains the data that will be used in the Node.js backend, relationships of ladder logic code to regular programming code. Given by the client. 
<h3>Node.js</h3>
<h4>CreateLLInstructs</h4>
Takes MS SQL Data and creates each instruction of ladder logic in a looping fashion like a list structure. 
<h4>InstructTyping</h4>
Correctly identifies what item from the database is a sequence, a step, or a control module. 
<h4>InstructLimits</h4>
Nodes can only connect to certain items, so a check if capable is required. 
<h4>DownloadtoPLC</h4>
Eventually, after creating a configuration, the user will want to send it to a PLC machine. 
<h4>LoginDetails</h4>
Login to the system to protect the work done. 
<h3>React Flow</h3>
<h4>MainUI</h4>
This is what the browser would call to display.
<h4>ButtonToolbar</h4>
The click and quickly done buttons at the top of the application, like download/export to PLC as an example. 
<h4>WorkSpace</h4>
This is the backdrop to where nodes will be put into to create a set of instructions.
<h4>NodeConnection</h4>
A visual to show what can and cannot connect on the workspace.
<h4>ProjectViewSide</h4>
As someone called it the folder structure of the workspace, it directly links to knowing what the workspace knows with the connected nodes.
<h4>NodeInstructions</h4>
Created in the backend, all of the individual instructions will be displayed to the right as a visual drag to the workspace. 
<h3>Browser</h3>
Pulls React Flow from its source to display in a webpage. 
