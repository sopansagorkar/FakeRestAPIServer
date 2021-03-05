# FakeRestAPIServer

## Step-1:
Download node js, refer below link:
[NodeJS Download](https://nodejs.org/en/download/)

Open a command prompt (or PowerShell), and enter the following:
```
node –v
```

The system should display the Node.js version installed on your system. You can do the same for NPM:
```
npm –v
```
For above two commands you should get response as below :

```
C:\Users>node -v
v10.16.3

C:\Users>npm -v
6.9.0
```

## Step:2
```
npm install -g json-server
```

## Step-3

Create a json file as db.json and open cmd in that path
Define the json format:
```
{
  "employees": [
    {
      "id": 1,
      "first_name": "sidharth",
      "last_name": "shukla",
      "email": "sidharth@automationreinvented.com"
    },
    {
      "id": 2,
      "first_name": "Steve",
      "last_name": "smith",
      "email": "steve@automationreinvented.com"
    },
    {
      "id": 3,
      "first_name": "virat",
      "last_name": "kohli",
      "email": "virat@automationreinvented.com"
    }
  ]
}
```

## Step-04:

Run the below command from command prompt
```
json-server --watch db.json
```

## Step-05:

By Default it will take localhost:3000, Now we can open URL http://localhost:3000/employees in the browser


## Step-06:
How to test in Postman?


Just open postman tool and ru below URI:


It's possible to extend URLs with further parameter. E.g. you can apply filtering by using URL parameters like you can see in the following:

```
http://localhost:3000/employees?last_name=shukla
http://localhost:3000/employees?first_name=sidharth
http://localhost:3000/employees/1
```

Validate the status code and response body.

## Step-07:

The following HTTP endpoints are created automatically by JSON server:

```
GET    /employees
GET    /employees/{id}
POST   /employees
PUT    /employees/{id}
PATCH  /employees/{id} 
```
So all the above methods can be tested both from Postman or Rest Assured.
