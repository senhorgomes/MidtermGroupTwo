# Workflow

Today we covered workflow in app development and github.
We also covered your ERDs, Wireframes, and Userstories.

## First step?

The first step would be to establish a database. Create a schema and some seeds so you can have a small set of data to work with the app.
At most, you would want 3 seeds, however you can create more later on.

- Schema
 - Create your tables
- Seeds
 - Testing
 - 3 users, 3 maps, 3 favs, 3-6 points

## Next step and the rest of the app workflow

Now that we've covered all the intial steps of the app development process. Let's talk about the workflow for the upcoming days. A lot of this will come from breaking down bigger problems into smaller problems.
Ideally, you would want to work in this flow:
- Backend
- Frontend
- CSS
- Repeat

Here is a better idea of how to go about each part:

- Backend → Create one route or a group of routes that fetch for data. (Example: routes for maps) First create the SELECT or INSERT statement for the query, and test it in in psql. Later you're going to want to test it out with express by create a GET or POST route and making a db.query. What you can try to do is create a route that runs a query and console logs the results. Test it out, and if it works, you're ready for the next part.

- Frontend → Now that the backend is ready, we're going to see if we can connect it to the Frontend. See if you can display the maps in your view via json. Then add html,(templateVars) and see if the maps still display or show via console.log. You would then continue on and see if you can click a button to display all maps, or via console.log. From there you can continue to flesh out the Frontend view.

- Css → Add some basic styling, maybe some bootstrap too. Later you can flesh out the app even more with more styling, fonts, to fully establish the image of the app.

What should happen is each group member should be always working on a part of the app. Once one member is done with the backend of one part, they should move onto another set of routes while someone else is working on the frontend.

## Reminder! NO LOGIN OR REGISTER ROUTES

These will be stretch features, instead what you'll be doing is as simple as setting a cookie with a user id if needed.
For example, you can set a different user as logged in by making a get request to /login/1, or /login/2.

## Git workflow

Whenever you are working on a new feature, please create a new branch. 
When you’re merging to main, please make it a group meeting so you can deal conflicts. (merge conflicts)