# Course Catalog Project API

### This It is a REST API using the NodeJS framework Express.  

# Update - this project is being used for the API and is hosted separate from the client. 

### hosted at tbd 

This API provides a way to administer a school database containing information about users and courses. Users can interact with the database to create new courses, retrieve information on existing courses, and update or delete existing courses. 

To make changes to the database, users will be required to log in so the API will also allow users to create a new account or retrieve information on an existing account.

## *Notes* 

- Run `npm install` to install the project. 
- Run `npm start` to start the server.
- Project is currently running on port 5000 
- This project contains two models - `Course` and `User` that are associated with one another. 
    - `Course` is a many to one model and `belongsTo` `User`.
    - `User` is a one to many model and `hasMany` associations for each user.
- `userId` must be specified for every `Course` when creating or updating a course.
- `routes.js` contains all the routes for creating, viewing (all or one at a time), updating users.  
- `routes.js` contains all the routes for all the routes for creating, viewing (all or one at a time), updating courses.
- `authenticate` contains all the **authentication** middleware to authenticate the following routes:
    - `GET` a list of all users
    - `GET` a specific user
    - `POST` a new course (note, this needs the inclusion of a `userId` in the request). 
    - `PUT` update an existing course.
    - `DELETE` a specific existing course.

- **bcrypt.js** is used to hash the passwords put into the database and to decrypt passwords in user authentication using compareSync.
- All routes have been tested in **Postman** using the file `RESTAPI.postman_collection.json`

