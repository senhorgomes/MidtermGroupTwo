# Planning

For your midterm you will want to spend as much time as possible planning the app before coding it. This is to ensure you have a solid vision of what you want to build. By planning, you are also preventing yourself from backtracking and having to rebuild major components of the app. 
Here are a couple things you should do for planning:

# Listing out the requirements for the app

All in a google doc.


## What are user stories?

In software development and product management, a user story is an informal, natural language description of features of a software system.


## Wikimaps
MVP
- As a user, I want to be able to create a map with my favourite coffee shops // CREATE => POST /maps
- As a user, I want to be able to edit the maps I create

Stretch goals
- As a user, I want to have a 3D model of the map, something like VR

If we're done with the app a week before, then you can work on implementing stretch features


## Prototype(MVP)

MVP, minimal viable product. An app that does the bare minimum and meets the requirements

How many of the user stories, are requirements?

Stretch → Things that we want to work on after the MVP is done.

## ERD 

- Entity Relationship Diagram. How the tables are connected together, it will define your database
What information will I need to get the features I want?
Tables, FK, PK

## Routes

You will not need to create a register page or a login page.
You can hardcode your login users.

/login/:id GET ROUTE
 -> /login/1
 -> A cookie with the id of 1 will be stored
 -> All pages would display and be used as user 1
/logout
 -> Clear the cookie and redirect

- CRUD
Maps
- Create -> /maps POST
- Read -> /maps or a single map /maps/:id
- Update ->
- Delete ->

Users
- Create -> /order POST
- Read -> /orders or a single order /order/:id
- Update ->
- Delete ->

## Wireframe

- Visuals of what the app would look like, and the flow of its content. Great websites for this would be [Figma](https://www.figma.com/), [Diagrams.net](https://www.drawio.com/), or any other tool you would like to use to draw

## Git Repo setup

We also went over the github repo setup.
Remember, only one person forks the LHL repo, and everyone else will clone that group members fork.
Example:
Group Member A forks the LHL repo, Group Member B and C will clone Group Member A's repo.
You will all be working out of one repo. You can invite people as collaborators for the repo by following this [guide](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)
Whenever you are working on a new feature, create a new branch. Please avoid working on the main branch as you may lose your work, or your other group members work

## Dividing up the workflow

[Trello](https://trello.com/) and Github provides tools for your group to organize the workflow of your app. You can see who is working on what, and what is left on the to-do list. You can leave notes for other group members as well.

# Node version

Stay on 16
nvm install 16
nvm alias default 16

Best of luck everyone!