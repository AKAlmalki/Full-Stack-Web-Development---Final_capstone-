# Movie Studio App

 In this app, we are trying to show you the movies with actors on it, so you can have better information about what actors are involved in this movie, what are the upcoming movies, and how many one of them is still acting in the new releases of the movies. However, you will get more infomation about the cinema world from this app.
 
 ## URL for the API
  Our API is hosted live via Heroku
 ```bash
 http://heroku.us.com
 ```
 
 ## Authentication Login URL
 
 There are three predefined users I have setup for you, you can use them to login into Auth0 and test the RBAC, they are different based on the Role. However, you have to logout to test the other user.
 
 #### Login Info:
 
 - Assistant:
   - email: assistant@gmail.com
   - password: Admin123
 - Director:
   - email: director@gmail.com
   - password: Admin123
 - Producer:
   - email: producer@gmail.com
   - password: Admin123

Each role have some permissions, see the following:

 - Assistant: 
   - Can view movies and actors
     - `get:actors`
     - `get:movies`
 
 - Director: 
   - All permissions a Casting Assistant has, Add or Delete actor, and modify actors or movies
     - `get:actors`
     - `get:movies`
     - `post:actors`
     - `delete:actors`
     - `patch:movies`
     - `patch:actors`
     
 - Director: 
   - All permissions a Casting Director has and Add or delete a movie from the database
     - `get:actors`
     - `get:movies`
     - `post:actors`
     - `delete:actors`
     - `patch:movies`
     - `patch:actors`
     - `delete:movies`
     - `post:movies`
 
 
 
 #### Login URL using Auth0
```bash
https://zshinoz.us.auth0.com/authorize?audience=movieStudioAPI&response_type=token&client_id=MMD81FKcgD0Mzek7TNCP6l2Tw7QVNVOC&redirect_uri=http://localhost:8080/login-results
```
 
 ### After Login
  After login, copy the access_token from url arguments, you will need it to test or use an API endpoint properly.
 
 Example of an access_token:
 ```
 eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IkliYkQ4THBuOGZYdy1PYkN4bWZOZSJ9.eyJpc3MiOiJodHRwczovL3pzaGlub3oudXMuYXV0aDAuY29tLyIsInN1YiI6ImF1dGgwfDYzM2E2NTA0ZmY2N2ZmYTVhNWVhYzNlNSIsImF1ZCI6Im1vdmllU3R1ZGlvQVBJIiwiaWF0IjoxNjY0Nzc2MjQ2LCJleHAiOjE2NjQ3ODM0NDYsImF6cCI6Ik1NRDgxRktjZ0QwTXplazdUTkNQNmwyVHc3UVZOVk9DIiwic2NvcGUiOiIiLCJwZXJtaXNzaW9ucyI6WyJkZWxldGU6YWN0b3JzIiwiZGVsZXRlOm1vdmllcyIsImdldDphY3RvcnMiLCJnZXQ6bW92aWVzIiwicGF0Y2g6YWN0b3JzIiwicGF0Y2g6bW92aWVzIiwicG9zdDphY3RvcnMiLCJwb3N0Om1vdmllcyJdfQ.ZT6tl-ybulM0nFMpJ2nEJiWv43RXC_nPnGF16s0qGetcfN3w0t8DF7AYvfzBedTf3n63QNXDNYUH1PssQ9YCNTPiqGW8t_jThLdsRsmW5iC8kExz27i5enESDuDq8LxVq42l54k2QB2oZz4tQ4SGwsl7nxPp9vQgQV2_rZPWTZo4euonTYMLTKYiCw2svDDsdfMC4lMTeUNimcEdJdxLJWGGyxr9u9Smgb3ZqxEoTfkJwa8FuK_47jTJTYJzUmjgNNMMfGXClGIG4eiD3WlZheryLQziQWcPV3gWM2I262II4HN0mVISUGWLxydzsrPxjYFZweOCwtyR-DEIfDk3yw
 ```
 
 `NOTE`: you can go to `jwt.io` website to see the content of this token.
