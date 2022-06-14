# AngularWithASP.NetCoreWebAPI-CRUD-MYSQL
 This repository contains Web App built on Angular 5 that interacts with WebAPI which has MySQL database


### Prerequisites

- Node.js
- Angular CLI
- .NET Core Framework

Settings are located in [appsettings.json](WebApi/appsettings.json). Change `insert_here` to your own keys.
 
- ConnectionString
- JWT SecretKey
- Email/SendGridAPIKey [how to create SendGrid?](https://docs.microsoft.com/en-us/azure/sendgrid-dotnet-how-to-send-email)

### Code-first database migration

Generate database `dotnet ef migrations add InitialMigration` then `dotnet ef database update`

### Run project

Run `ASPNETCORE_Environment=Development dotnet run` to build project.

## Functionality Overview

### Features

* Cross Platform
* CRUD operations
* Entity Framework Core MySQL
* JWT Authentication
* Swagger API documentation
* Responsive Design

### Page navigation

- **Home**
    - **Home** ../
        - article list with infinite scrolling
        - the most popular tags
        - user leaderboard
    - **Dependencies** ../dependencies
        - static page
        - information about used frameworks and third party libraries
    - **Contacts** ../contacts
        - static page
- **Auth**
    - **SignIn** ../auth/signin
        - store JWT token in localStorage
    - **SignUp** (/auth/signup)
        - Email verification
- **Idea**
    - **Add new** ../idea/new
        - Auth guard (redirects if user is not logged)
        - edit list of tags
        - article editor WYSIWYG
    - **Details** ../idea/:id
        - like/dislike button
        - raw html render
        - favorite button
        - edit/restore button
        - comments section
    - **Search** ../idea/search/:value
        - search by value in title and article
- **Profile**
    - **User info** ../profile/:username
        - information about user
        - list of favorited articles
        - list of created articles
    - **Settings** ../settings
        - edit avatar
        - change username

## Built With

* **ASP.NET Core 2.0 WebAPI**
* **Angular 5**
* **MySQL**

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
