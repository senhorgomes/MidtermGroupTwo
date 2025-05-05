# Workflow

Today we covered workflow in app development and github.
We also covered your ERDs, Wireframes, and Userstories.

## First step?

The first step would be to establish a database. Create a schema and some seeds so you can have a small set of data to work with the app.
At most, you would want 3 seeds, however you can create more later on.

- Schemas

- Test database
 - Small sample, maybe 3 seeds for each table
 - 3 Users, 3 stories (One for each user, one of them being complete), 3 constributions (One story with 2, and one story with one), have more than 3 seeds for your likes table

 - Run the command \i *file name*

 - 01_users.sql
 - 02_stories.sql
 - 03_contributions.sql
 - 04_likes.sql

## Next step and the rest of the app workflow

Now that we've covered all the intial steps of the app development process. Let's talk about the workflow for the upcoming days. A lot of this will come from breaking down bigger problems into smaller problems.
Ideally, you would want to work in this flow:
- Backend
- Frontend
- CSS
- Repeat

Each member works on a feature

  - Backend/Frontend/CSS 
  - Backend/Frontend/CSS

Here is a better idea of how to go about each part:

- Backend → Create one route or a group of routes that fetch for data. (Example: routes for maps) First create the SELECT or INSERT statement for the query, and test it in in psql. Later you're going to want to test it out with express by create a GET or POST route and making a db.query. What you can try to do is create a route that runs a query and console logs the results. Test it out, and if it works, you're ready for the next part.

- Frontend → Now that the backend is ready, we're going to see if we can connect it to the Frontend. See if you can display the maps in your view via json. Then add html,(templateVars) and see if the maps still display or show via console.log. You would then continue on and see if you can click a button to display all maps, or via console.log. From there you can continue to flesh out the Frontend view.

- Css → Add some basic styling, maybe some bootstrap too. Later you can flesh out the app even more with more styling, fonts, to fully establish the image of the app.

What should happen is each group member should be always working on a part of the app. Once one member is done with the backend of one part, they should move onto another set of routes while someone else is working on the frontend.

## Reminder! NO LOGIN OR REGISTER ROUTES

These will be stretch features, instead what you'll be doing is as simple as setting a cookie with a user id if needed.
For example, you can set a different user as logged in by making a get request to `/admin`.
Restaurant view will be `/`

## Git workflow

Whenever you are working on a new feature, please create a new branch.

- feature/name-of-feature
 Once you're done with a branch, you then merge it into main
After adding and commiting and pushing our changes to feature/orders

git checkout main
git pull origin main <- This allows your main branch to have the latest code on main
git pull origin feature/orders <- This allows you to merge your branch onto main
git add . & git commit again
git push origin main <- Then we push the changes onto Github main

- fix/name-of-bug or name-of-feature-update

When you’re merging to main, please make it a group meeting so you can deal conflicts. (merge conflicts)


# Backend
Will include all your routes (GET and POST routes), all your schema and seeds, and all necessary db queries.
Some routes will only return data, some routes will render a page.
- Look at what data you need for each page to render fully or fufill a functionality (Menu items)
- Next, create SQL queries to render that information/perform that action -> For the frontpage create an sql query that grabs all menu items -> `SELECT * FROM menu_items;`
- Once we have created the SQL query, we're going to test it in psql, simply by running it.
- Create a dbQuery function in our app, create a new file called `menu.js`
```
const getMenuItems = () => {
 db.query('SELECT * FROM menu_items;')
.then(data => return data.rows)
}
```
What is being returned is an array of objects
- We can create our route
```
const express = require('express');
const router  = express.Router();
const menuQueries = require('../db/queries/menu');

router.get('/', (req, res) => {
  menuQueries.getMenuItems()
    .then(menuItems => {
      //Once you have the view for this page, you can switch it to res.render('homepage');
      res.json({ menuItems });
    })
    .catch(err => {
      res
        .status(500)
        .json({ error: err.message });
    });
});

module.exports = router;
```
- Then we can test it and move onto other routes
