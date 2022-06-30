### My-Social-API by Gerard Mennella

# Summary
An API for social media applications using mongoDB. It includes routes for users, friends, thoughts, and reactions.

# Code Breakdown

## Models
### Thoughts
The Thought.js file contains the schemas for thoughts and reactions. The thoughts schema requires a username and text for the thought. it also contains the timestamp for its creation and an array of reactions accompanied by a virtual for the reaction count. The reaction schema also requires a username and text for the body. It uses a timestamp for its creation as well, these timestamps are formatted using the dateFormat.js file in the utils folder.
### User
The User.js file contains the schema for a user. The user schema requires a username and email address. the email address is validated using the validator npm package. It also contains arrays for a user's friends and thoughts, as well as a virtual for the friend count.

## Controllers
### Thought Controller
The thought controller contains the CRUD logic for the thought routes. There is logic to create a thought, get all thoughts, get one thought, edit a thought, and delete a thought. There is also logic to add and remove reactions to the thoughts.
### User Controller
The user controller contains the CRUD logic for the user routes. There is logic to create a user, get all users, get one user, edit a user, and delete a user. There is also logic to add and remove friends to and from a user.

## Routes
### Thought Routes
The thought-routes.js file imports the functions from the thought-controller.js file and assigns them to the proper endpoints.
### User Routes
The user-routes.js file imports the functions from the user-controller.js file and assigns them to the proper endpoints.

## Server
The server.js file creates the express server, connects it to the mongoDB database, and requires the routes.

# Video Walkthrough
[Walkthrough](https://drive.google.com/file/d/1OSnJquY4fJB0QnFz4LoToGR4GLCByJTH/view)