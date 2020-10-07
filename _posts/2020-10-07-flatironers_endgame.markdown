---
layout: post
title:      "FlatIroners:Endgame"
date:       2020-10-07 10:08:36 +0000
permalink:  flatironers_endgame
---


The final portion of the Flatiron curriculum featured a crash course in React and Redux. React allows for considerable powerful and interactive applications with very little start up time. This is in large part thanks to so much 'magic' going on behind the scenes. From Babel, webpack, to the 'virtual dom', React has some serious capabilities as it's disposal right out of the box. Redux on the other hand in the manner Flatiron attempts to teach is the polar opposite. Cumbersome, diffiult to set up, and offers arguable very little if any benefit for smaller scale projects.

With this project I went outside of the curiculum and attempted to learn React 'Hooks' as well as the Redux/Toolkit. Both of which proved incredibly useful and rewarding. While React Hooks are not designed to replace class based components of traditional react applications they do provide quite a nice benefit in the form of an easier access to state and lifecycle method in the form of useEffect(). The Redux/Toolkit is the biggest benefit.

The Toolkit is actually designed and stated in its documentation to be the standard way to write redux code going forward. It's much easier to set up and removes a lot of the tedious or repetitive steps  from vanilla redux. You can actually implement redux without questioning the meaning of the human condition for once. It's an extremely powerful that should definitely become a part of the FlatIron curriculum in the future. 

As for my project it takes data from the corona virus api and a new api to give readily available statistics on a country by country basis when users click they can access any news articles available. They can like an article that will toss a post request to the back end to store it for future use. Otherwise nothing is saved without user input. All the corona stats are pulled fresh upon start up.
