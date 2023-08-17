# Workflow

Today we covered workflow in app development and github.
We also covered your ERDs, Wireframes, and Userstories.

## Strengths

A great way to start with app development is establishing your strengths, and what part of the app would you want to work on.

Russell, Lanre, Rauber -> Backend

Russell, Lanre, Rauber  -> Frontend

 -> API

Lanre -> CSS

## First step?

The first step would be to establish a database. Create a schema and some seeds so you can have a small set of data to work with the app.
At most, you would want 3 seeds, however you can create more later on.

1 user
4 categories
8 items/ 2 per category

## Next step and the rest of the app workflow

Now that we've covered all the intial steps of the app development process. Let's talk about the workflow for the upcoming days. A lot of this will come from breaking down bigger problems into smaller problems.
Ideally, you would want to work in this flow:
- Backend
- Frontend
- CSS/API
- Repeat

Here is a better idea of how to go about each part:

- Backend → Create one route or a group of routes that fetch for data. (Example: routes for categories) First create the SELECT or INSERT statement for the query, and test it in in psql. Later you're going to want to test it out with express by create a GET or POST route and making a db.query. What you can try to do is create a route that runs a query and console logs the results. Test it out, and if it works, you're ready for the next part.


- Frontend → Now that the backend is ready, we're going to see if we can connect it to the Frontend. See if you can display the categories in your view via json. Then add html,(templateVars) and see if the categories still display or show via console.log. You would then continue on and see if you can click a button to display all items, or via console.log. From there you can continue to flesh out the Frontend view.

- Css → Add some basic styling, maybe some bootstrap too. Later you can flesh out the app even more with more styling, fonts, to fully establish the image of the app.

![workflow](https://github.com/senhorgomes/MidtermGroupThree/blob/main/devops.png)
What should happen is each group member should be always working on a part of the app. Once one member is done with the backend of one part, they should move onto another set of routes while someone else is working on the frontend.

## Reminder! NO LOGIN OR REGISTER ROUTES

These will be stretch features, instead what you'll be doing is as simple as setting a cookie with a user id if needed.
For example, you can set a different user as logged in by making a get request to login/:id, /login/1, or /login/2.

## Git workflow

Whenever you are working on a new feature, please create a new branch from main. 
When you’re merging to main, please make it a group meeting so you can deal conflicts. (merge conflicts)

If you're merging a branch into main
git checkout main
git pull origin main -> Maybe someone pushed some changes onto the main branch
git merge feature/login
git push origin main

For your next feature
git branch feature/newMap