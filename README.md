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

A logical explanation of all my architectural choices in the project
I tried to keep the architecture of my code as clean and reusable as possible.
For the front-end Part:
Basically, I used the command "npx create-react-app TicTacToe" to make the directory setup. It setup React App basic structure of file in the directory with name TicTacToe
But the components folder wasn't present 
I thought making too many scattered files will mess up my real motive to keep clean as possible so I made a component folder in SRC this will keep all used modules that are an important features of my code
package.json will keep all dependencies as a register record that will show all dependencies used and as I mentioned just a command is enough to install all of that ealier
Now back-end part
I created the architecture from scratch, and while practicing I experienced having a messy app.js (main file) so this time I should look for best practises I found that we can use folders like modules, routes, middleware and a db file that will keep database connection promise.
I've added lots of comments in code that help to understand the code and problems I faced during /while making the project

The major issue was Usually localhost and 127.0.0.1 are synonyms but  lately, they have changed the localhost to be an ipv6 address so unless your services are configured to understand ipv6 addresses they will not work 

It almost made me give up but somehow after searching too much and finally discussing it with a senior developer I was able to solve it.
