## #Endpoints

## #Post Endpoints

## Path Method Request Response ResponseCodes Description

"/posts" GET NONE Post[] 200, 404 Get all posts
"/posts/{id}" GET int Id Post 200, 404 Get post by id
"/posts/user/{id}" GET int UserId Post[] 200, 404 Get posts by user id
"/posts/category/{id}" GET int CategoryId Post[] 200, 404 Get posts by category
"/posts" POST Post NONE 201, 400 Create new post
"/posts/{id}" PUT int Id, Post NONE 200, 404 Update post
"/posts/{id}" DELETE int Id NONE 200, 404 Delete post

---

## User Endpoints

## Path Method Request Response ResponseCodes Description

"/users" GET NONE User[] 200, 404 Get all users
"/users/{id}" GET int Id User 200, 404 Get user by id
"/users/email/{email}" GET string Email User 200, 404 Get user by email
"/users" POST User NONE 201, 400 Create new user
"/users/{id}" PUT int Id, User NONE 200, 404 Update user info
"/users/{id}" DELETE int Id NONE 200, 404 Delete user

---

## Category Endpoints

## Path Method Request Response ResponseCodes Description

"/categories" GET NONE Category[] 200, 404 Get all categories
"/categories/{id}" GET int Id Category 200, 404 Get category by id
"/categories" POST Category NONE 201, 400 Create new category
"/categories/{id}" DELETE int Id NONE 200, 404 Delete category

---

## Comment Endpoints

## Path Method Request Response ResponseCodes Description

"/posts/{postId}/comments" GET NONE Comment[] 200, 404 Get all comments for post
"/comments/{id}" GET int Id Comment 200, 404 Get comment by id
"/posts/{postId}/comments" POST Comment NONE 201, 400 Create new comment
"/comments/{id}" PUT int Id, Comment NONE 200, 404 Update comment
"/comments/{id}" DELETE int Id NONE 200, 404 Delete comment

---

## Entities

ApplicationUser : IdentityUser
Property Name Data Type Description

---

FirstName string First name of user
LastName string Last name of user
FullName string Full name of user
Address string Street address of user
Zipcode string Zip code of user
City string City of residence
Region string Region of residence of user
Country string Country of residence of user
Role string Role of user

---

## Post

Property Name Data Type Description
Id int Id of post in database
Title string Title of post
Content string Content of post
AuthorId int Id of the user who created the post
CategoryId int Id of the post category
CreatedAt datetime Date and time of post creation
UpdatedAt datetime Date and time of last update

---

## Category

Property Name Data Type Description
Id int Id for database
Name string Name of category in database

---

## Comment

Property Name Data Type Description
Id int Id of comment in database
PostId int Id of the post the comment belongs to
AuthorId int Id of the user who created the comment
Content string Content of comment
CreatedAt datetime Date and time of comment creation
UpdatedAt datetime Date and time of last update

---
