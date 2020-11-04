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
- Pre-requisites or Dependencies (Defined Below)

## Role

- Currently are there are two Roles defined.
- User
  - Update Profile
  - Search Profile
  - Use Recommeder to find parnter
- Admin
  - Manage Users

## Schema

<h4><b>Users Schema</b></h4>

| Name                  | Type      | Required | Unique | Encrpyted |
| --------------------- | --------- | -------- | ------ | --------- |
| firstname             | String    | Yes      | No     | No        |
| email                 | String    | Yes      | Yes    | No        |
| gender                | String    | Yes      | No     | No        |
| password              | String    | Yes      | No     | Yes       |
| photourl              | String    | Yes      | No     | No        |
| peronaldetails        | Reference | Yes      | No     | No        |
| recommendationdetails | Reference | Yes      | No     | No        |
| type ( Role )         | String    | Yes      | No     | No        |
| isVerfied             | Bollean   | Yes      | No     | No        |
| isActive              | Bollean   | Yes      | No     | No        |

<h4><b>Personal Details Schema</b></h4>

| Name       | Type      | Required |
| ---------- | --------- | -------- |
| middlename | String    | No       |
| lastname   | String    | Yes      |
| religion   | String    | No       |
| DOB        | String    | Yes      |
| age        | Number    | Yes      |
| phoneno    | String    | No       |
| education  | String    | No       |
| user       | Reference | No       |

<h4><b>recommendation Schema</b></h4>

| Name      | Type            |
| --------- | --------------- |
| user      | Reference       |
| religion  | Array of Object |
| minage    | Number          |
| maxage    | Number          |
| education | Array of Object |

<h5><b>religion Object</b></h5>

```bash
  religion: [{
      name: {
        type: String,
      },
      count: {
        type: Number
      }
    }]
```

<h5><b>education Object</b></h5>

```bash
  education: [{
      name: {
        type: String,
      },
      count: {
        type: Number
      }
    }],
```

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
