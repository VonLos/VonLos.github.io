---
layout: post
title:      "The Neverending Journey-Sinatra Project"
date:       2020-07-08 10:52:41 -0400
permalink:  the_neverending_journey-sinatra_project
---

I remember our cohort lead, Jenn Hansen, mentioning in the early days that Sinatra was when a lot of people started to feel like proper web developers. After finishing this project I'm rather inclined to agree. It was challenging, but very enlightening. By combining my CLI  application's use of an API and building a website to persist data pulled from it, what I've created is a simplified version of the MAL website. It uses a standard model, view, and controller deisgn. I found it rather interesting being able to blend html and ruby code using `<%`. This allowed my views display to be so much more dynamic and interactive for a user. The mvc model was another part I quite like for this project. There was very clear seperation of concerns and the project almost became like a clock. Each piece going together to create a functioning whole. Every part having a clear function and design when building it. The was some additional refactoring neccessary in order to properly adhere to restful conventions. After all the net would be a wild wild place if there was not some semblance of order in the form of RESTful conventions. MAL is a text book example of restful conventions in many ways.

MAL is a website that acts as a both of database for all things anime and a resource for viewers to create their own lists. In other words the perfect site to base a sinatra project off of as that translates very nicely to MVC format. There was a bit of difficulty with active record, but ultimately my project allows users to search up a variety of information regarding any anime that is in the mal site itself and persist it as their own personal list. 

Looking at MAL from a RESTful standpoint https://myanimelist.net/anime/31964/Boku_no_Hero_Academia just a basic link show's how it adheres. Type of object being edited, the unique database ID of said object, and finally a name. Honestly, that was most useful part of this section and project. Most people never stop to look at an actual url besides the basic ******.com. Our jobs as web developers would be significantly more difficult if RESTful convetions had never taken off. By exenstion the user experience would also have suffered consdierably. Ultimately this project has instilled a measure of gratitude for the mvc and restful designs.



