Tool using 
- API Tools - Postman /Newman
- Mobile Android Emulator = LeapDroid
- API URL captured = Telerik Fiddler
- Documentation reference = https://developer.todoist.com/rest/v8/


Task 1 - Test “Create Project”
--------------------------
1. Test “Create Project”

Steps:POSTMAN API
Create test project via API.
- Login via todoist using tokken
https://github.com/anitanasirun/TaskAssignmentSetel/blob/master/Image%20Screenshot/Image1.png?raw=true
API Request :  
[Get]  https://beta.todoist.com/API/v8/projects?token=3a962c29757fdf1d2cf0d11d8ecc42d669b87c7c

Test Code : 
var responsedata = JSON.parse(responseBody);

//Checkpoint: Status Code is 201
tests["Status code is 200"] = responseCode.code === 200;

//Checkpoint: Check the ResponseBody displayed
tests["Body contains id"] = responseBody.has("id");
tests["Body contains name"] = responseBody.has("name");
tests["Body contains order"] = responseBody.has("order");
tests["Body contains indent"] = responseBody.has("indent");
tests["Body contains comment_count"] = responseBody.has("comment_count");

//console.log ("id", responsedata.id);


- Create test Project 



MOBILE APP -Login into mobile application.
- Screenshot attached 
Verify on mobile that project is created
- Screenshot attached






