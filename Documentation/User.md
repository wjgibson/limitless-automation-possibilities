![BaseApp](https://user-images.githubusercontent.com/38050891/200923734-0afe86cd-d763-4e52-8d1a-a23f9ac88d5d.png)
<h1>1: The Sidebar</h1>
<h2>This sidebar is interactable with 6 draggable items able to be dropped into area 4</h2>
<p>
The indicator for selection will not change when hovering over a sidebar item. For example, click to grab an Input Node and the click can be released anywhere to the left of the sidebar. Also for example, when this Input Node is dropped, it creates input node with a black dot to signify a potential connection. All 6 items follow the same logic.
</p>
![Inputonsidebar](https://user-images.githubusercontent.com/38050891/200931382-5a2c5a76-604e-47fd-9da2-294a499aecc9.png)
<p>Will not drop into area 4</p>
![image](https://user-images.githubusercontent.com/38050891/200935491-49613488-ccae-48a7-861f-6d3987022a41.png)
<p>Will drop into area 4</p>
<h3>Input Node</h3>
![image](https://user-images.githubusercontent.com/38050891/200935983-c54c9dd4-b649-40f4-91e1-a5a265c7bdd5.png)
<p> When Input Node is dropped </p>
<h3>Sequence </h3>
![image](https://user-images.githubusercontent.com/38050891/200952471-f36e2fb5-5dc0-46d7-904a-7a7c74ef27c4.png)
<p> When a Sequence is dropped </p>
<h3>Step</h3>
![image](https://user-images.githubusercontent.com/38050891/200952531-42638a04-acf4-48e2-8961-cd3ef1e458a8.png) 
<p> When a Step is dropped </p>
<h3>Control Module</h3>
![image](https://user-images.githubusercontent.com/38050891/200952606-4b2045cd-5f98-4583-a700-b3327f11b49d.png)
<p>When a Control Module is dropped </p>
<h3>Caste 2 Sequence</h3>
![image](https://user-images.githubusercontent.com/38050891/200952681-23b8240e-132f-4360-b7f7-449487b16336.png)
<p> When a Caste 2 Sequence is dropped </p>
<h3>Output Node</h3>
![image](https://user-images.githubusercontent.com/38050891/200952806-1213b44c-61bc-4c03-8df8-145725005226.png)
<p> When Output Node is dropped </p>
<h1>2:Save/Restore</h1>
<h2>With what is on area 4, save and restore affects that space. Area 4 can be empty but that is not the intended use for the save feature. </h2>
<p> Click save which brings up a popup at the top of the browser for naming the current set of nodes on the workspace</p>
![image](https://user-images.githubusercontent.com/38050891/200958945-d07bcd69-cbf9-463a-8e51-8ba0f8a9552d.png)
<p> After entering a name and clicking OK, the current set of nodes on the workspace can be changed however seems fit. To restore to some previous point that was saved, click restore which pops up the restore configuration popup. </p> 
![image](https://user-images.githubusercontent.com/38050891/200961169-8d7eeee1-7b17-47d6-9e27-fc0e4290df3e.png)
<p><b>Important</b>, the name given when restoring must have been named with the save feature or no action will occur. Also, it must be the same browser instance between saving and restoring a configuration, due to the configuration being saved in local storage of the browser. </p>
<h1>3: Zoom, Fit View, and Lock Interactivity</h1>
<p> The plus symbol will zoom in the workspace/area 4, The minus symbol will zoom out the workspace/area 4. </p>
![image](https://user-images.githubusercontent.com/38050891/200971738-600009c1-06b3-4a05-886a-6ec5734f98db.png)
<p>An example image</p>
![image](https://user-images.githubusercontent.com/38050891/200972484-b9d93e52-c1b8-45b9-962c-8f1822ce1db8.png)
<p>Zoom out pressed</p>
![image](https://user-images.githubusercontent.com/38050891/200972551-3c1f20fc-8c52-4a22-88ba-8ba5c91273dd.png)
<p>Zoom in pressed to revert the zoom out</p>
<p>Fit view aligns nodes in the workspace so that they are more centralized in view.</p>
![image](https://user-images.githubusercontent.com/38050891/200973009-1e6b4ef7-e198-425a-9b21-e1034dd0b737.png)
<p>Example image</p>
![image](https://user-images.githubusercontent.com/38050891/200973274-39bff743-26af-4d06-a2e2-cde2a6592e75.png)
<p>Corrected view image</p>
<p> The lock features disables the interactions for the area 4/workspace which are also the functionalities of the workspace being to delete nodes and connect nodes together. 
<h1>4:Workspace</h1>
<h2>The workspace does the removal of nodes, allows for redragging of nodes, and to connect nodes together.</h2>
<p>For the removal of nodes, click the node and the frame will get darker to show selection, then press backspace to remove the node.</p>
![image](https://user-images.githubusercontent.com/38050891/200978290-5deb0321-6eef-48f6-a5da-71e58f0e3b63.png)
<p>Unfocused node</p>
![image](https://user-images.githubusercontent.com/38050891/200978346-7eae40cf-ac52-4320-abfe-632d930f2b5d.png)
<p>Focused node</p>
<p>To connect nodes together, drag from the black circle to an appropriate corresponding black circle</p>
![image](https://user-images.githubusercontent.com/38050891/200979061-3cf52c1e-6746-49cf-9db9-4d91b7f76c33.png)
<p>An example image to show a line of connections that will fail to connect on the left, to the right will connect due to correct ordering of nodes. </p>
  


  
  
