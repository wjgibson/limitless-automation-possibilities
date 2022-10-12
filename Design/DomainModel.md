<h2>Link to LucidChart</h2>

https://lucid.app/lucidchart/c8ea3a16-8abd-414f-ae6b-4863f05ae97d/edit?viewport_loc=69%2C-43%2C1227%2C799%2C0_0&invitationId=inv_1ae13b6a-96de-440b-8661-21264cc1c404#

<img width="1616" alt="Architecture" src="https://user-images.githubusercontent.com/89548120/195460509-e805be82-9e83-49a9-98e7-33c63b5bf884.png">

<h2>User</h2>
  In the domain, the user will be the automation engineer who is programming the configuration for the PLC. This will be what all requirements and use cases are for. It will also hold the login information for the user.
  <h2>Workspace</h2>
  In the domain, the workspace will be where the user is dragging the nodes to. It will contain the node structure as a json document.
<h2>Node</h2>
  In the domain, the node will hold the information of what was pulled from the database. It will also hold internally, the id of it's parent and any children.
<h2>Database</h2>
  In the domain, the database is what holds all of the information the program needs to run. Instead of the webapp directly downloading to the PLC, or adding sequences and steps to a configuration, the database will do all of that. No PLC logic will be rewuired for the webapp. Only an API to call the database logic
