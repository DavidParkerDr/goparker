---
title: (R)evolving Art
author: David Parker
date: 2012-07-25T13:14:00+00:00
tags: ["art", "Genetic Algorithm", "Silverlight"]
---
Though I like to think that my software development work shows a little artistry, I am certainly not an artist in the classical sense of the word. However, I have been developing an art project with artist Roberto Bono (<a href="http://www.arteutile.net/rob/artist.htm" target="_blank">Roberto&#8217;s website</a>) for the past year or so, and as I have just uploaded a couple of new Roberto works I thought I would share them.

The ‘idea’ of the work is that is is comprised of 12 double sided paintings that form the whole. You are able to arrange the individual parts in any configuration that you like leading to a very large number of combinations.

<div style="margin:0;display:inline;float:none;padding:0;" id="scid:8747F07C-CDE8-481f-B0DF-C6CFD074BF67:44ac4670-0f08-4795-a6f6-621a91770be5" class="wlWriterEditableSmartContent">
  <a href="http://lh6.ggpht.com/-mdoXch4eCuM/UA_w_keU9FI/AAAAAAAAAIA/fQhyIh_SI08/roberto3a-8x6.png?imgmax=800" title="A random configuration of the piece" rel="thumbnail"><img border="0" src="http://lh6.ggpht.com/-Rd6bVaDn75g/UA_xAg3IG6I/AAAAAAAAAII/9uOJrEQMF3E/roberto3a%25255B9%25255D.png?imgmax=800" width="580" height="483" /></a>
</div>

I developed the <a href="http://www.daviusmaximus.karoo.net/squares/" target="_blank">web application</a> in Silverlight and at the basic level it allows the user to configure the paintings by rotating, flipping, and moving each individual piece. You are also able to randomise the configuration and there is a slideshow mode that periodically calls the randomise method. If you find a configuration that you like you can save it to your PC (as an XML configuration file) and reload it later.

Another feature that you can mess around with, is an implementation of a genetic algorithm which, in theory at least, will evolve the configurations to maximise the colour match across the joins between the pictures.

<div style="margin:0;display:inline;float:none;padding:0;" id="scid:8747F07C-CDE8-481f-B0DF-C6CFD074BF67:c9f7a921-8cc6-4ca6-a131-0d8c573fb000" class="wlWriterEditableSmartContent">
  <a href="http://lh4.ggpht.com/-eilTdVFIZ_k/UA_xBpvS5eI/AAAAAAAAAIQ/HuwMNVD5t4g/roberto3rect-8x6.png?imgmax=800" title="The web application interface" rel="thumbnail"><img border="0" src="http://lh3.ggpht.com/-aNk14zpsaY4/UA_xCVPKEnI/AAAAAAAAAIY/IsEfNK4yD3U/roberto3rect%25255B3%25255D.png?imgmax=800" width="580" height="440" /></a>
</div>

<a href="http://www.arteutile.net/alberti/alberti.htm" target="_blank">Andrea Alberti</a> is a musician and composer who, using the ‘Roberto 3’ piece as inspiration (select it from the settings <a href="http://www.daviusmaximus.karoo.net" target="_blank">here</a>) put together a music work to accompany it. There is a longer piece of music that continuously plays whilst the painting is visible and there are additional sounds and snippets that play when certain paintings are manipulated. It makes for a rather interesting experience I think.