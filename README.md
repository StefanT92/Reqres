# Reqres
Reqres API test project

1. Download ReqRes.postman_collection.json as well as user-data.csv and put it in the same folder
2. Install newman tool on the following way:
    - prerequisites is to have node.js installed
    - open node.js command prompt and type following command: npm install -g newman
3. For running ReqRes.postman_collection.json from the node.js command line, make sure you are in the appropriate directory where collection and user-data.csv are located:
    - in the node.js command line type the following command: newman run ReqRes.postman_collection.json -d user-data.csv
    
Final result will be presented also in the table form:

![image](https://user-images.githubusercontent.com/101990378/159373534-b241f85d-334a-43c6-a92d-c1daafc9c97c.png)

4. In order for tests to be executed every 24h from command line, for Windows OS, Task Scheduler application can be used:
    - Open Task Scheduler application, create a new task and give it an arbitrary name.
    - Check radio button "Run whether user is logged on or not"
    - At the bottom choose "Configure for" appropriate Operation system
    - Click on Triggers tab and add New trigger
    - Set new trigger to Begin the task "On a schedule"
    - Check radio button "Daily"
    - Choose start time and date and click OK
    
     ![image](https://user-images.githubusercontent.com/101990378/159375216-c03de548-ddbd-4c5b-a9c8-029d735f7962.png)
     
    - Click on Action tab and Choose a path that navigates to the command prompt, for example: "C:\Windows\System32\cmd.exe" "newman run ReqRes.postman_collection.json"
    - Add arguments:  -d user-data.csv
