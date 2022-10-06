<h1>Architecture</h1>
This project will be a monolithic architecture as the project will mostly be JS Frameworks with a database as well. C# could be a replacement to Node.js but we think the current idea will be easier to communicate together. 
<h2>Drawing</h2>
<img width="1152" alt="Architecture" src="https://user-images.githubusercontent.com/38050891/194359416-07f49ba2-0911-4a82-b8d4-b352156f2b31.png">
<h3>MS SQL Database</h3>
Contains the data that will be used in the C# backend, relationships of ladder logic code to regular programming code.
<h3>Node.js \ C# Backend</h3>
Takes MS SQL Data and creates the necessary steps to call some node or one direction of ladder logic. Continues with creating these nodes until all actions of ladder logic needed are made. 
<h3>React Flow</h3>
Creates the visual for nodes, allowing for drag and drop technology. Connects steps of ladder logic together in a sequential order.
<h3>Browser</h3>
Pulls React Flow from its source to display in a webpage. 
