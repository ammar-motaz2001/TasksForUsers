# 1-How To Run Project 

```
npm init -y
npm i express mysql2
npm i {package_name}
npm i nodemon  //to save all changes continuously
```
# 2- How to initilization DataBase
1-DB_HOST='bxtahtqtgwm9jkjptlo7-mysql.services.clever-cloud.com'
2-DB_NAME='bxtahtqtgwm9jkjptlo7'
3-DB_USERNAME='uxucpekdpgaqdt6m'
4-DB_PASSWORD='gbr5QLAcHeDel3gQuYty'
5-Create TABLE Tasks and Users
6- I used Sequalize (ORM) So don't need to access ForeignKey becouse Sequalize do it .
### Note: Knowing that I did not use process.env.DB_... to make it easier for you to read it and to easily identify the database.

# 3-How I divide My Project 
1- database Folder contain db_Connection and models Schema (TaskModel ,User Model) 
2- Middleware 
3- modules ( task Model have : task Controller ,task Router , user Model have : user controller , user Router) 
4-utils ( Error Handling ) 

# 4- Expected Output For all End Points : 
### Sign In 
```
{
    "message": "Success",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjIzLCJlbWFpbCI6ImFtbWFyMjJAZ21haWwuY29tIiwicm9sZSI6InVzZXIiLCJpYXQiOjE3MjA1MzI5MTJ9.NacIGgOGEYKNtrmkI5mjVNCtyJs6Ry083We5iJtAkpI"
}
```
### Sign Up 
```
{
    "message": "Signed Up Successfully",
    "user": {
        "role": "user",
        "id": 41,
        "name": "ammar Motaz",
        "email": "ammar220@gmail.com",
        "updatedAt": "2024-07-09T13:49:35.791Z",
        "createdAt": "2024-07-09T13:49:35.791Z"
    }
}
```
#### Note :If Email Exist The output is : 
```
{
 "message": "Email Already Exist"
}

```
### Add Task 
```
{
    "message": "success",
    "task": [
        {
            "status": "Pending",
            "id": 111,
            "title": "Task9999",
            "description": "a",
            "userId": 23,
            "createdAt": "2024-07-09T13:51:48.402Z",
            "updatedAt": "2024-07-09T13:51:48.402Z"
        }
    ]
}
```
### Get All Tasks
```
{
    "message": "success",
    "numofTasks": 1,
    "AllTasks": [
        {
            "id": 111,
            "title": "Task9999",
            "description": "a",
            "status": "Pending",
            "createdAt": "2024-07-09T13:51:48.000Z",
            "updatedAt": "2024-07-09T13:51:48.000Z",
            "userId": 23,
            "user": {
                "id": 23,
                "name": "ammar Motaz",
                "email": "ammar22@gmail.com",
                "role": "user",
                "createdAt": "2024-07-08T06:57:13.000Z",
                "updatedAt": "2024-07-08T06:57:13.000Z"
            }
        }
    ]
}
```
