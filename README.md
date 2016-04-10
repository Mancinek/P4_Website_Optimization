#Website_Optimization

This is a recreation of classic arcade game **Frogger**. It is simplified version with easy rules. At this stage,
this game has no end, you can collect points endlessly. This repository gives you basis to further development of game.

##Contents

1. How to run
2. How to play
3. Issues
4. How the code is organized
5. Links

##How to run

To run this game [download](https://github.com/Mancinek/frontend-nanodegree-arcade-game/archive/master.zip) the repository and open the `index.html` file in your browser - the game will start immediately.

##How to play

You are the character

### How to move the player

Use _arrows_ o

### Rules

You hav

##Issues

There is one

##How the code is organized

The game runs on basis of three _js_ files:

* `engine.js` draws the canvas on the screen and provides the game loop functionality by calling update and render methods on player and enemies instances (defined in app.js)
* `resources.js` is an image loading utility and caching layer
* `app.js` implements _Player_, _Enemy_ and _Gem_ classes. It creates also _Settings_ class to adjust game difficulty.

The repository contains also other helper files like:

* images of characters, water, grass, stones,
* `index.html` that loads the scripts on the page,
* `style.css` that defines the style of html (centers the canvas and score).

##Links

The basic engine of the game is forked from Udacity repository [here](https://github.com/udacity/frontend-nanodegree-arcade-game).
