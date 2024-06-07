### **Rest student details API Testing with Postman Newman**
This project demonstrates API testing using Postman, providing a collection of tests to validate various endpoints of the API. 

### **Features**

- Tests for GET, POST, PUT, DELETE requests
- Collection of tests covering different API endpoints
- Environment setup for easy switching between environments
- Pre-request scripts for data setup
- Test scripts for assertions and validations

## API Documentation:
-(https://documenter.getpostman.com/view/34581585/2sA3XJkQ2u)
  
### **Technology used:**
- Postman
- Newman

### **Prerequisite:**
- Node Js
- Newman
- Newman Html Report Library

### **Installation**

1. Postman: If you haven't already, [download and install Postman.](https://www.postman.com/downloads/)
2. Clone the repository:
 ```console 
  git clone (https://github.com/fahima22/API_testing_newman_report.git)
```
3. Import the Postman collection:
    - Open Postman.
    - Click on the Import button.
    - Select the file from the repository.
4. Import the Postman environment:
    - In Postman, click on the gear icon in the top right corner.
    - Select **Import** and choose the file.
5. Newman and Report Installation Process:
    - Newman Install Command:
     ```console 
      npm install -g newman
    ```
    - Newman Html Report Install Command:
     ```console 
      npm install -g newman-reporter-htmlextra
    ```
### **Usage**
1. Select Environment:
    -   In Postman, select the appropriate environment (e.g., Development, Production) from the top-right dropdown.
3. Run Collection:
    -   Select the imported collection from the Collections sidebar.
    -   Click on the Runner button to open the collection runner.
    -   Select the desired environment.
    -   Click Start Test to run the collection.
8. View Results:
    -   Once the tests are complete, view the results in the Runner tab.
    -   Detailed test results can be viewed for each request.

## **Testing**

## Test Case Scenarios:

## _**1. Create Student_Details*_

### Base URL:https://thetestingworldapi.com 
### Request URL:baseUrl/api/studentsDetails
### Request Method: POST
### Pre-request Script:
```console 
   var firstName = pm.variables.replaceIn("{{$randomFirstName}}");
pm.environment.set("FirstName", firstName);

var lastName = pm.variables.replaceIn("{{$randomLastName}}");

var middleName = firstName + lastName;
pm.environment.set("MiddleName", middleName);

pm.environment.set("LastName", lastName);

var year = Math.floor(Math.random() * (2050 - 1980 + 1)) + 1980;
var month = Math.floor(Math.random() * 12) + 1;
month = (month < 10) ? '0' + month : month;
var day = Math.floor(Math.random() * 28) + 1;
day = (day < 10) ? '0' + day : day;
var dateOfBirth = day + '/' + month + '/' + year;
pm.environment.set("DateOfBirth", dateOfBirth);



```
  **Request Body:** 
 ```console 
 {
    "first_name": "{{FirstName}}",
    "middle_name": "{{MiddleName}}",
    "last_name": "{{LastName}}",
    "date_of_birth": "{{DateOfBirth}}"
}
```
  **Response Body:**
 ```console 
  {
    "id": 10288004,
    "first_name": "Golda",
    "middle_name": "GoldaSchuster",
    "last_name": "Schuster",
    "date_of_birth": "14/10/1982"
}
```
 ## _**2. Get All Student Details**_
### Request URL:  baseUrl/api/studentsDetails
### Request Method: GET
### Response Body:
 ```console 
[
    {
        "id": 10288004,
        "first_name": "Golda",
        "middle_name": "GoldaSchuster",
        "last_name": "Schuster",
        "date_of_birth": "14/10/1982"
    },
    {
        "id": 10288003,
        "first_name": "prathap",
        "middle_name": "rana",
        "last_name": "dasari",
        "date_of_birth": "22-08-1994"
    },
    {
        "id": 10288002,
        "first_name": "sample string 1",
        "middle_name": "sample string 2",
        "last_name": "sample string 3",
        "date_of_birth": "sample string 4"
    },
    {
        "id": 10288001,
        "first_name": "Furkan",
        "middle_name": "A",
        "last_name": "Simsek",
        "date_of_birth": "07/02/1996"
    },
    {
        "id": 10288000,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287999,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287998,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287997,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287996,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287995,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287994,
        "first_name": "Testing",
        "middle_name": "K2",
        "last_name": "Worold",
        "date_of_birth": "12/12/2000"
    },
    {
        "id": 10287993,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287992,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287991,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287990,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287989,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287988,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287987,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287986,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287985,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287984,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287983,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287982,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287981,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287980,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287979,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287978,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287977,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287976,
        "first_name": "Testing",
        "middle_name": "K",
        "last_name": "Worold",
        "date_of_birth": "12/12/1995"
    },
    {
        "id": 10287974,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287973,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287972,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287971,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287970,
        "first_name": "Salman",
        "middle_name": "",
        "last_name": "Khan",
        "date_of_birth": "14/10/1996"
    },
    {
        "id": 10287969,
        "first_name": "Ajit",
        "middle_name": "Kumar",
        "last_name": "Singh",
        "date_of_birth": "14/02/1997"
    },
    {
        "id": 10287968,
        "first_name": "Salman",
        "middle_name": "",
        "last_name": "Khan",
        "date_of_birth": "14/10/1996"
    },
    {
        "id": 10287967,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287966,
        "first_name": "Ms.",
        "middle_name": "Maximus",
        "last_name": "Price",
        "date_of_birth": "2088-06-06"
    },
    {
        "id": 10287964,
        "first_name": "Wilmer",
        "middle_name": "sample string 3",
        "last_name": "Hane",
        "date_of_birth": "2030-06-06"
    },
    {
        "id": 10287963,
        "first_name": "Bernice",
        "middle_name": "sample string 3",
        "last_name": "Hodkiewicz",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287962,
        "first_name": "Belle",
        "middle_name": "sample string 3",
        "last_name": "Gutkowski",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287961,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287960,
        "first_name": "rishabh",
        "middle_name": "bhardwaj",
        "last_name": "sharma",
        "date_of_birth": "20-04-1996"
    },
    {
        "id": 10287959,
        "first_name": "John",
        "middle_name": "K",
        "last_name": "Manchester",
        "date_of_birth": "1/4/1989"
    },
    {
        "id": 10287958,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287957,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287956,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287955,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287954,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287953,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287952,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287951,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287950,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287949,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287948,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287947,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287946,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287945,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287944,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287943,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287942,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287941,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287940,
        "first_name": "John",
        "middle_name": "K",
        "last_name": "Manchester",
        "date_of_birth": "1/4/1989"
    },
    {
        "id": 10287939,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287938,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287937,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287936,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287935,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287934,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287933,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287932,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287931,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287930,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287929,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287928,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287927,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287926,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287925,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287924,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287923,
        "first_name": " shakir1122",
        "middle_name": " mairaj3222",
        "last_name": " mufti4333",
        "date_of_birth": " 1992"
    },
    {
        "id": 10287922,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287921,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287920,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287919,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287913,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287910,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287909,
        "first_name": "Hugh",
        "middle_name": "Eveline",
        "last_name": "Huels",
        "date_of_birth": "12.12.1990"
    },
    {
        "id": 10287908,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287907,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287906,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287905,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287904,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287903,
        "first_name": "sample string 2",
        "middle_name": "sample string 3",
        "last_name": "sample string 4",
        "date_of_birth": "sample string 5"
    },
    {
        "id": 10287902,
        "first_name": null,
        "middle_name": null,
        "last_name": null,
        "date_of_birth": null
    },
    {
        "id": 10287901,
        "first_name": "Cordie",
        "middle_name": "CordieVeum",
        "last_name": "Veum",
        "date_of_birth": "23/12/2033"
    },
    {
        "id": 10287900,
        "first_name": "Dudley",
        "middle_name": "DudleyLabadie",
        "last_name": "Labadie",
        "date_of_birth": "14/03/2024"
    },
    {
        "id": 10287899,
        "first_name": "Helene",
        "middle_name": "HelenePurdy",
        "last_name": "Purdy",
        "date_of_birth": "22/11/1990"
    },
    {
        "id": 10287898,
        "first_name": "Furkan",
        "middle_name": "A",
        "last_name": "Simsek",
        "date_of_birth": "07/02/1996"
    },
    {
        "id": 10287880,
        "first_name": "Salman",
        "middle_name": "",
        "last_name": "Khan",
        "date_of_birth": "14/10/1996"
    },
    {
        "id": 10287879,
        "first_name": "Ajit",
        "middle_name": "Kumar",
        "last_name": "Singh",
        "date_of_birth": "14/02/1997"
    }
]
```

 ## _**3. Get Specific Student Details**_
### Request URL: baseUrl/api/studentsDetails/id
### Request Method: GET
### Pre-request Script:
  **Response Body:**
 ```console 
  {
    "status": "true",
    "data": {
        "id": 10288004,
        "first_name": "Golda",
        "middle_name": "GoldaSchuster",
        "last_name": "Schuster",
        "date_of_birth": "14/10/1982"
    }
}
```


newman run Rest_Student_Details_API.postman_collection.json -e Rest_Student_Details_API.postman_environment.json
- Run Command for Report: 
```console 
newman run Rest_Student_Details_API.postman_collection.json -e Rest_Student_Details_API.postman_environment.json -r cli,htmlextra
```

## Newman Report Summary:
![Newman Report Summary] (https://github.com/fahima22/API_testing_newman_report/blob/main/Report/Rest_Student_Details_API-2024-06-06-03-42-05-464-0.html)
![image] (https://prnt.sc/NwuLIA86saRp)
![Newman Report Summary] (https://prnt.sc/ywOCzD11zKGM)
