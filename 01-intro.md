---
layout: post
status: draft
title: Grid-based browser games
author:
  display_name: Nathan
  email: n@demick.org
date: 2023-09-11 10:21:38 -0400
categories:
- games
comments: []
---
Ever since regular people have had casual access to computing resources, they have written game programs. _(insert aside about [Spacewar! on PDP-1](https://en.wikipedia.org/wiki/Spacewar!))_ I'm sure we could discuss at length the psychology of play, and why electronic games are so compelling. My own theory is that writing game programs fulfills an innate creative need for world-building. There's just something about setting up rules for an interactive environment, and seeing the simulation conform to those rules, that gives one a sense of power and achievement. Game programming falls on the rebellious side of the dichotomy of computing; resources are used for whimsy and fun, as opposed to Serious Business and Making Money (although sometimes these ideas intersect).

The explosion in popularity of the internet created a new platform for software. With the first generation of web browsers, these programs were fairly primitive &mdash; data needed to be saved and displayed by a web server, and any user interaction required a full page refresh cycle. I played a number of games that used this style.

As JavaScript became standardized across browsers, more and more web software shifted computing responsibility from the "back-end" to the "front-end." _(discuss Flash)_ This included games, of course. One new web standard that was added to browsers was the `<canvas>` element, which lots of folks used for games. It basically offers a bitmap that can be drawn on programmatically. This is great for games, as it mimics what you might use in a computer game running "natively" &mdash; i.e. outside a web browser. The canvas can even be drawn on using 3D programming techniques, via WebGL.

The only problem with using `<canvas>` for a game is that you throw away two of the traditional building blocks of the web &mdash; HTML and CSS. I've always enjoyed (ab)using technology in ways unintended by the original use case, and want to merge two of my interests &mdash; games and web pages. One of the solutions I've found for this conundrum is to _keep_ HTML and CSS, and use them for a game's graphics. This simplifies a few things for the developer.

1. If you have a background in web development, HTML and CSS should be tools that you already know. Conversely, if you don't have prior experience, learning these tools has real-world benefits outside of game-making &mdash; for example, my day job is in web development, which includes laying out user interfaces using HTML/CSS.

2. Loading game graphics can be handled by the browser. Define backgrounds for HTML elements in CSS, and the files are loaded automatically.

3. CSS transforms and transitions can be used to manipulate game objects, rather than needing to write or import your own tweening functions.


why web-based games?

1. games are fun
2. instant gratification for users; no install necessary
3. low commitment in a sandboxed environment
4. fun to bend the rules of what is essentially a glorified document viewer
5. the skills/techniques used are transferrable to other web development endeavors
6. easy to use browser abstractions for update loops and user input

why grid-based games?

1. many game programming concepts are easier with a grid
   a. collision detection is just checking if an (x,y) coord is truthy or falsey
   b. easy to update only the cells that have changed
   c. mouse/touch input is dead simple to map to a grid
   d. lots of games can be "deconstructed" to a grid
