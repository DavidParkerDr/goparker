---
title: Ultimate King Domino
date: 2018-05-14
tags: ["boardgame", "3d printer", "optimisation"]
---
![alt text](/img/post_images/180514_kingdomino_tiles.png "Printed Tiles")

Just a few days before last Christmas I began belatedly thinking about what sort of things I could do with my family during the holiday period. A little while ago, one of my buddies had introduced me to Kingdomino (https://boardgamegeek.com/boardgame/204583/kingdomino) which is a fun tile placement game for up to 4 players. It was on 'the list' of games that I had put together after perusing a number of sources on the internet for games that play well with three players. This is because my immediate family unit is made up of me, my wife, and our (currently) 9 year old son.

I mentioned that I was belatedly thinking about it because I started after even Amazon's Christmas delivery cut off. This might be an obstacle for your average fellow, but armed with my 3D printer I was not deterred.

<!--more-->

I decided to model (in Sketchup) and print my own version of the game. It required 48 'domino' tiles, as well as some additional tokens. In the proper version of the game, each of the tiles has some lovely illustration on it depicting the various realms of the kingdom (such as woodland, ocean, farms etc.). However, the core of the game surrounds  choosing and arranging the tiles to ensure that tiles of the same type are bundled together (all ocean tiles are touching, for example). This is because the scoring is done by multiplying the number of contiguous tiles of the same type by the number of scoring crowns (in the original game and pips in my version). It is pretty abstract already, and I just took it another notch closer to 11. So instead of oceans and farms, mine are stars and hearts and other assorted simple shapes. As long as the combination of shapes on tiles matched the combination of realms in the original game, then they would be functionally equivalent.

So that was what I did, and it worked out quite well, though I made a bit of a mistake by punching the shapes all the way through the tile. This was a problem because you don't want to know what is on the other side of the tile until the time comes. To avoid reprinting them all, I stuck them all down to some nice shiny card which solved the problem. I also decided that the quick identification of the various pieces would be improved with colour coding. So I painted them all with my son's acrylic paints. It is definitely not a 'pro' job and you might be a little disappointed if it arrived in your Amazon order, but it worked pretty well from a functional point of view.

The game does play well with 3 players, but the mode that I have been enjoying the most is the 2 player version where you use all of the tiles available and build a 7 x 7 square grid of the tiles. There is still a random element to it as the tiles are shuffled so the order that you receive them (and have to fight with your opponent over) is different each game, but I like the fact that the game is not influenced by the presence (or not) of a particular tile.

A fun (if you like that sort of thing, and I do) extra stage that you can add to the game is that once you have totted up your scores, you rearrange your own tiles to see what the maximum score is that could have been made with that selection assuming optimal placement. This can be achieved by having no 'orphan' tiles and all the colours are kept together with no gaps. It is interesting to see where a player achieved close to the maximum possible with their tiles (near optimal placement during game play) and their opponent scored less during the game, but have a higher maximum possible score.

A idea that I thought would be useful related to this is a possible 'final' year project. An image recognition problem such that I can take a photo of the completed Kingdomino grid and have the computer (mobile device makes the most sense) add up the score for me. Lazy perhaps, but an interesting problem.

I am quite fond of winning (as opposed to the alternative) and I also enjoy puzzle solving and optimisation. So a question that has been sparking my interest that neatly encompasses these things is what is the maximum possible score given a free choice of tiles. During the game, you are fighting for tiles with your opponent, but if there is a optimal set then you could theoretically target that combo in a game scenario, especially if the selection is not obvious or intuitive.

| Colours        | Number of Tiles | Number of Spots | Total Points |
| -------------- |:---------------:|:-----:|:-----:|
| Blue Squares   | 22 | 6 | 22 x 6 = 132 |
| Grey Circles   | 26 | 5 | 26 x 5 = 130 |
| Pink Triangles | 18 | 6 | 18 x 6 = 108 |
| Yellow Stars   | 14 | 6 | 14 x 6 = 84 |
| Green Crosses  | 10 | 6 | 10 x 6 = 60 |
| White Hearts   | 6  | 10 | 6 x 10 = 60 |

The table describes the complete set of tile types and the maximum points available assuming that all the tiles of each colour are arranged together. However it is not quite as simple as that as each domino has two tiles on it which may be different colours. Also the points density is different for the different colours. For example, the blue squares when arranged together gives the player 132 points, whereas the white hearts only achieve 60 points. In a 7 x 7 grid there are 24 dominos (48 tiles) plus your starting castle. So if you focus on blue squares you use up half of your available space. That is before you consider that the colour combos on the dominos may force you to include some other colours.

![alt text](/img/post_images/180514_kingdomino.png "Highscore?")

The picture above shows my best yet. 267 points, including the bonus for having the central castle (10 points) and using all the tiles (5 points) This is calculated in the table below. Notice the disappointing placement of those stray blue squares. I ought to write a computer program to solve this problem... or I think that will set this as a future coursework assignment sometime as it is a fun optimisation problem, and then someone else can do the work for me.

| Colours        | Number of Tiles | Number of Spots | Total Points |
| -------------- |:---------------:|:-----:|:-----:|
| Blue Squares 1   | 2| 2 | 2 x 2 = 4 |
| Blue Squares 2   | 1 | 1 | 1 x 1 = 1 |
| Blue Squares 3  | 1 | 0 | 1 x 0 = 0 |
| Blue Squares 4  | 1 | 0 | 1 x 0 = 0 |
| Grey Circles   | 17 | 5 | 17 x 5 = 85 |
| Pink Triangles | 6 | 3 | 6 x 3 = 18 |
| Yellow Stars   | 7 | 6 | 7 x 6 = 42 |
| Green Crosses  | 7 | 6 | 7 x 6 = 42 |
| White Hearts   | 6  | 10 | 6 x 10 = 60 |
| Central Castle   |   |  | 10 |
| Used all tiles   |   |  | 5 |
| **total**   |   |  | 267 |

Can you do better? Consider the gauntlet thrown.
