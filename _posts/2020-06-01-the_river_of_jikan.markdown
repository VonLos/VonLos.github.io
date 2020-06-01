---
layout: post
title:      "The River of Jikan"
date:       2020-06-01 15:05:59 +0000
permalink:  the_river_of_jikan
---


For better or worse my CLI showed a lot about who I am as a person and a programmer. Jikan translates to time and this project is something I want to continually evolve with time. I view this as a starting point, not a final product. In terms of minimum product viability and project requirements, sure it meets those. However in regards to my end vision it most certaintly does not. What this project has shown me is just how wide and long the path I walk is. It's also given me a glimpse of what lies toward the end and renewed my drive to further my development. As for the project itself let's get into it.

The Jikan API Tool (Fantastic name I know!) is a CLI gem that allows users to interactive with the... Jikan API. My Anime List or "Mal" as it's commonly refered to, is a popular site for any information regarding that medium. However they have consitently and somewhat understandbly refused to make an official API. Enter to the stage Jikan! Jikan scrapes Mal to return the information I wanted access to. However due to the sheer amount of information Mal posses from voice actors to studios and even mangaka's the actual endpoint of the api was nebulous. So I had to find a way to pull user input from my CLI class to my API call methods. Since the end point of data would very based on what the user wanted to search. I managed to create a relatively decent chain from my start up menu function in the CLI class requesting user input as needed until returning the desired results. Editing the results was another probrlem in of itself.

The results themselves was actually stored in a bit messy nested array and hash combination. At least compared to some of the simpler ones I had user prior. So iterating down to access the results and then instiating a new class object for each result entry was a bit difficult. It did however make me extremely thankful for the extensive lesson's on hashes and arrays that Flatiron provided. Ultimately, after taking in user input and pulling data from the API users are then asked to decide if they want further information. Currently it only allows for searches regarding anime and returns the first five results. This was partly done to avoid triggering any limits and requesting too much. As well as to keep the data and console clean for a basic beginning.

What really excites me is the framework laid here. There's so much potential and so many features I want to add already. This has become something I'll return to later and continue to develop personally.


