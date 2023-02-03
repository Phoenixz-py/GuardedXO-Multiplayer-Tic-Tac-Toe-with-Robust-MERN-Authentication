# TicTacToe-Intern-Quest
A web game made with MERN

Introduction:
This is a MERN Full Stack-based project made solely for Assignment Round for internship. It's a game of multiplayer tic-tac-toe which can be accessed only when someone is a user or register & login themselves to play it. Without this, they can't access the game.
The whole Authentication was done with hashing, JWT & salt to make it very secure if the database was hacked. User stay logged in until we logout or clear the cache.

To Run:

The running is very simple as I have added package.jason to have a record of different dependencies so the code runner or someone trying to run my code just have to enter the command "npm install" it will install all dependencies 
Since I have both server and client  I figured out to use "concurrently" npm and added  "both": to the scripts below in package.json 
```js
"scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "both": "concurrently "npm run start" "nodemon backend/index.js""
  }
```
Now all that is left to do is "npm run both"
And the live server is ready with the client and server running at 3000 and 5000 respectively
