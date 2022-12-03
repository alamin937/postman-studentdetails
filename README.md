# postman-studentdetails
# API Testing
* Api testing is the frontend and the database communicate to each other they are not directly communicate middle sight the server work and the api serve the data frontend to the database and get the data from database to the frontend and show the information.
* Using Postman for API tesing
* Report Generate using the NewMan ( Globali Install the Newman) 
<!DOCTYPE html>
<html>
<head>
</head>
<body>
 <h1>How done by the api testing</h1>
  * First Create the collection <br>
  * Then create the add request option <br>
  * Using the Method (Post, Get, Put and Delete) <br>
  * Post Method Use Insert the Data <br>
  * Get Method Use get the specific user by the id number <br>
  * Put method updated the specific information using by id <br>
  * delete method delete the specific user using by the id
  <h1>Using the Test Option in postman</h1>
  * Crate the Enviorment <br>
  * the test option write the javascript code and every api used variable send to the environment and use this data dynamically <br>
  * Write the Test Case in Test option <br>
  * checking the data are wrong or correct <br>
  var jsonData = pm.response.json()

pm.environment.set("id", jsonData.id)

var code = responseCode.code

if(jsonData.first_name == pm.environment.get("FirstName")){

    pm.test("FirstName", function () {
        pm.expect(jsonData.first_name).to.eql(pm.environment.get("FirstName"));
    });
}
<br>
if(jsonData.middle_name == "anik"){
    pm.test("middlename", function(){
        pm.expect(jsonData.middle_name).to.eql("anik");
    })
}
<br>
if(jsonData.last_name == pm.environment.get("LastName")){
    pm.test("lastname", function(){
        pm.expect(jsonData.last_name).to.eql(pm.environment.get("LastName"));
    })
}
<br>
else{
    console.log("not Mached");
}
<br>

* Using the Pre-request Script
<h1>Newman</h1>
  Install Command: npm install -g newman <br>
Run Command: <br>
newman run “Path/CollectionName.json” -e Path/EnvironmentName.json <br>
newman run “Collection Link” -e “Path”/EnvironmentName.json <br>

Report: <br>
Install: npm install -g newman-reporter-html <br>
	npm install -g newman-reporter-htmlextra <br>
Run Command: <br>
newman run “Collection Link” -e EnvironmentName.json -r cli,html <br>
newman run “Collection Link” -e EnvironmentName.json -r cli,htmlextra <br>

<h1>Tests</h1>
<img width="100%" src="https://i.ibb.co/c2q14j1/Screenshot-1.png" alt="Girl inhh a jacket">

<h1> Pre Request Script </h1>
<img src="https://i.ibb.co/bWJmKHB/Screenshot-2.png" alt="Girl in a jacket">

<h1> Report </h1>
<img src="https://i.ibb.co/PmNL5Y0/Screenshot-4.png" alt="Girl in a jacket">

</body>
</html>
