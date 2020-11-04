# Matrimonial-Website

```
yarn start
```

It will run under the url http://127.0.0.1:3000/

Email and Password for Online Website:<br>

- Admin
  - Email : admin@gmail.com
  - Password : admin
- Users
  - 1
    - Email : salamkhan@gmail.com
    - Password : salamkhan
  - 2
    - Email : kareena@gmail.com
    - Password : kareena
  - 3
    - Email : akshay@gmail.com
    - Password : akshay

## Pre-requisites

- Node JS (Tested on v12.14.0)
- MongooseDB
- MongooseDB Compass (Optional)

## Role

- Currently are there are two Roles defined.
- User
  - Update Profile
  - Search Profile
  - Use Recommeder to find parnter
- Admin
  - Manage Users

## Directory

```bash
|___ Root
|   |--- app.js
|   |
|   |--- Procfile ( Heroku File )
|   |
|   |--- .env ( Enviroment File )
|   |
|   |--- config
|   |    |--- db.js
|   |    |--- utils.js
|   |
|   |--- Controller
|   |    |--- index.js
|   |    |--- recommendation.js
|   |    |--- users.js
|   |
|   |--- Dump (Mongoose Dump) (Dump)
|   |
|   |--- middlewares
|   |    |--- middleware.js
|   |
|   |--- Models
|   |    |--- personaldetails.js
|   |    |--- recommendation.js
|   |    |--- users.js
|   |
|   |--- Public
|   |    |--- css (Static)
|   |    |--- images (Static)
|   |    |--- script
|   |    |    |--- bootstrap.min.js
|   |    |    |--- datatables.js
|   |    |    |--- datatables.min.js
|   |    |    |--- editprofile-js.js
|   |    |    |--- home-js.js
|   |    |    |--- loginandregister.js
|   |    |    |--- manage_user-js.js
|   |    |    |--- searchpage.js
|   |
|   |--- router
|   |    |--- index.js
|   |    |--- Handlers
|   |         |--- admin.js
|   |         |--- user.js
|   |
|   |--- views
|   |    |--- partials
|   |    |    |--- navbar.ejs
|   |    |
|   |    |--- adddetails.ejs
|   |    |--- editprofile.ejs
|   |    |--- home.ejs
|   |    |--- index.ejs
|   |    |--- manage_people.ejs
|   |    |--- searchpage.ejs
|   |    |--- user.ejs
```
