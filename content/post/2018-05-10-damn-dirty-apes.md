---
title: Damn Dirty Apes
date: 2018-05-10
tags: ["threethinggame", "spooky elephant", "monogame"]
---
![alt text](/img/post_images/180510_damn_dirty_apes.png "Damn Dirty Apes")

So Three Thing Game (http://threethinggame.com/post/2018-05-05-the-event/) took place last weekend and much fun was had by all. That link was an article I wrote chronicling the event including all the winners. There were a number of other great games made that didn't place and hopefully they will all make their own blog posts about it because this is my blog so I want to talk about the great game that I made.

<!--more-->

Spooky Elephant is the game 'studio' that is made up of a loose collective of lecturers and friends to create games at game jams and beyond (though mostly at Three Thing Game). We have made low double figures number of games over the last 8 years or so and I am hoping to do a series of posts documenting them soon. One of them even won a prize in a national competition which significantly contributed to my being allowed to get an XBox One (gift voucher and strong negotiating with my wife). So naturally Spooky Elephant should now be referred to as an award winning game studio.

Anyway, dragging the narrative back to the present, last weekend Spooky Elephant once again took part in Three Thing Game and as is customary we received three 'thing' theme words with which to inspire our game. These were:

### ape, sewer, and animated.

Animated was handy, and finally spurred me on to make a useful generic and reusable spritesheet class. What usually happens is that we cobble something together on a case by case basis for all of our character objects which is far from ideal. So this time I made something that I loosely based on the spritesheets that we used as part of the now defunct Playstation Mobile SDK back when we made the Ballrus (more on that in a later blog post). The key aspect that I took from there is that you can define the details of the spritesheet in an Xml file that can be loaded in by the spritesheet object to define the image file(s) and 'tag' them so that you can specify the 'idle' sequence for example.

As for sewer, that provided our setting as the natural habitat of the apes that would be the player characters. 

"So what is the game?" I hear you ask. Well, we didn't finish it, so it is missing a bunch of game play, but essentially the idea was a couch multiplayer style game where the apes could run around the sewers and collect bananas. Also in the sewers are the spooky elephants. They don't eat bananas but spread the team colours which would confer a speed bonus when running on their own colour. Also there would likely be some kind of multiplier bonus at the end for the team with the most colour spread about.

A short video captures a little bit of the look and feel of it, though obviously an actual game is still pending.

{{< youtube lEdTs8_2y_E >}}

We plan on polishing it somewhat (and adding the game play) before releasing it to various platforms so watch this space.