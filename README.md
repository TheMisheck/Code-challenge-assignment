# Code-challenge-assignment
Attached is angular front end with Spring boot back end assignment
To run the angular prohject, you need to instal node modules package by running npm i in your terminal
The spring boot project has inco-oporated security features, and to hit any endpoint, tou need to include the token as a bearer.
On first running of the app, it will genereta tables and insert username and password set at demoBankApplication.java
please uncomment the commented lines to enable this for the first time you run the app.
The base URL is : http://localhost:9200/api
                  other endpoints will followthe base url for example to hit sign in, navigate to /signIn to hit customers navigate 
                  to /customers    -----any other endpoint created will follow suit

http://localhost:9200/api/auth/signIn

{
	"username" : "admin",
	"password" :"admin"
}


{
    "username": "admin",
    "email": "info@metropol.com",
    "firstName": "Admin First Name",
    "middleName": "Admin Middle Name",
    "lastName": "Admin Last Name",
    "token": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsInNjb3BlcyI6IlVTRVIiLCJpYXQiOjE1NjU2NTU2MDgsImV4cCI6MTU2NTY3MzYwOH0.xd25a21r8X4ZDhIFIBnU4qJItx6Tn4tXlK7RjsyERSE"
}



