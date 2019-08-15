# Code-challenge-assignment
Attached is angular front end with Spring boot back end assignment
To run the angular prohject, you need to instal node modules package by running npm i in your terminal
The spring boot project has inco-oporated security features, and to hit any endpoint, tou need to include the token as a bearer.
On first running of the app, it will genereta tables and insert username and password set at demoBankApplication.java
please uncomment the commented lines to enable this for the first time you run the app.
The base URL is : http://localhost:9200/api
                  other endpoints will followthe base url for example to hit sign in, navigate to /signIn to hit customers navigate 
                  to /customers    -----any other endpoint created will follow suit --- please click edit of this ReadMe file to have a text view of the sample requests and outputs: 

Method: POST
URL: http://localhost:9200/api/auth/signIn

Body:
{
	"username" : "admin",
	"password" :"admin"
}

Response:
{
    "username": "admin",
    "email": "info@metropol.com",
    "firstName": "Admin First Name",
    "middleName": "Admin Middle Name",
    "lastName": "Admin Last Name",
    "token": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsInNjb3BlcyI6IlVTRVIiLCJpYXQiOjE1NjU2NTU2MDgsImV4cCI6MTU2NTY3MzYwOH0.xd25a21r8X4ZDhIFIBnU4qJItx6Tn4tXlK7RjsyERSE"
}

Method: POST
URL: http://localhost:9200/api/customers
Body: 
{
"dateOfBirth": " Tue Aug 13 2019 00:00:00 GMT+0300",
"designation": "ZXC",
"email": "aa@ymail.com",
"employerName": "SKDMM",
"employerPhone": "ZXC",
"employerPhysicalAddress" : "XCZXC",
"employerPostalAddress" : "XZCZ",
"employerTerms": "permanent",
"firstName": "m xzcm ",
"homeAddress": "zxmckm",
"idNumber": "32323",
"lastName": "mx cm ",
"maritalStatus": "married",
"membershipNumber": "5656",
"numberOfDepedants": 54,
"phoneNumber": "0714852147",
"physicalAddress": "222 ELD",
"staffNumber": "2553"
}

Response:
{
    "updatedAt": null,
    "createdAt": "2019-08-15T21:19:34.378+0000",
    "deletedAt": null,
    "membershipNumber": "5656",
    "firstName": "m xzcm ",
    "lastName": "mx cm ",
    "dateOfBirth": " Tue Aug 13 2019 00:00:00 GMT+0300",
    "idNumber": "32323",
    "maritalStatus": "married",
    "numberOfDepedants": "54",
    "homeAddress": "zxmckm",
    "phoneNumber": "0714852147",
    "physicalAddress": "222 ELD",
    "employerName": "SKDMM",
    "employerPhysicalAddress": "XCZXC",
    "employerPhone": "ZXC",
    "designation": "ZXC",
    "staffNumber": "2553",
    "employerTerms": "permanent",
    "_links": {
        "self": {
            "href": "http://localhost:9200/api/customers/99482385-aa8f-46bb-8f61-684c700014ee"
        },
        "customer": {
            "href": "http://localhost:9200/api/customers/99482385-aa8f-46bb-8f61-684c700014ee"
        }
    }
}

Method: POST 
URL: http://localhost:9200/api/customers/{customerId}/loans
Body: 
{
   "loanPurpose":"Development loan",
   "loanType":"emergency",
   "loanAmount":"120000",
   "bankName":"Faulu bank",
   "dateGranted":"2018-01-10T21:00:00.000Z",
   "repaymentPeriod":"2 years",
   "outstandingBalance":"13000"
}

Method: GET 
URL: http://localhost:9200/api/loans
Body:
{
    "_embedded": {
        "loans": []
    },
    "_links": {
        "self": {
            "href": "http://localhost:9200/api/loans{?page,size,sort}",
            "templated": true
        },
        "profile": {
            "href": "http://localhost:9200/api/profile/loans"
        }
    },
    "page": {
        "size": 20,
        "totalElements": 0,
        "totalPages": 0,
        "number": 0
    }
}



