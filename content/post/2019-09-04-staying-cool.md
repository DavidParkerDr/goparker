---
title: Staying Cool
date: 2019-09-04
tags: ["3d printer", "underextrusion"]
---

![alt text](/img/post_images/190904_going_badly.png "Going badly")
<br/>
A little while ago I was designing and printing an update to my printer to allow it to use one less motor for controlling the z-axis. The basic printer design uses two lead screws to raise and lower the x-axis. It still does, but now it only uses one motor to control both screws instead of the original two. But that is not what this post is about. Instead it is about staying cool under circumstances to drive one mad.

<!--more-->

A better start would be that I was designing and *trying* to print... I just couldn't figure out why the print was failing. It was producing a gorgeous first layer, but then after some indeterminant period of time on this multi hour print it would just fail. First with underextrusion, then with a full on clog.

I tried atomic pulls, which would allow me to unblock the nozzle and immediately start printing again, only to watch with increasing frustration as it failed again later. One particular source of annoyance was that it was seemingly random. Sometimes the symptoms appeared early, and sometimes it would be hours in.

It turned out that the issue that I was facing was cooling related. Apparently at some point, that I hadn't noticed before, the wire connecting to the little 30mm fan cooling the heatsink of the hotend had broken off. That meant that the heatsink was not being actively cooled so that heat could travel up the heatbreak. The consequence of this was that the usually rigid filament would become a little like cooked spaghetti (which is famously difficult to push) and would deform and compress in the hotend making it harder (underextrusion) and then impossible (clogged) to extrude. The time taken to fail was variable based on loads of factors like how long a gap it had to cool before trying to print again.

Annoyingly the wire had broken exactly where it met the fan circuit board which was inaccessible. Luckily I had an older fan from a previous incarnation of the printer so I swapped it out and resumed printing.

Fast-forward a few months and I am trying to print out some high-resolution models. Things are... not going well. It being a while since the previous issues had happened I had forgotten all about it and was repeating the frustrating atomic pull rituals in an attempt to get the print to complete properly. The same symptoms as before with seemingly random print fails following underextrusion and then nozzle clogs. 

The fan was still running. So it wasn't exactly the same as before. I thought that I found the issue (almost certainly also an issue) when I noticed that the heatbreak piece was loose in the heatsink. This would cause an improper thermal connection and reduce the ability of the heatsink to conduct away the heat. After tightening it, the problem seemed a little less, but I was still getting poor results from the print. 

After doing a little reading around I began to wonder if the fan that I replaced the broken one with was just a little pathetic and had insufficient puff. So I ordered a 'proper' replacement from the suppliers of the hotend as I really wanted to make sure.

Lo and behold, full beautiful service is resumed. 

![alt text](/img/post_images/190904_much_better.png "Much better")

So for my own future reference, if you are getting random underextrusion and then nozzle clogs, please check:

- The heatsink fan is running
- The heatbreak is not loose in the heatsink
- The fan has enough CFM puff (you haven't replaced it with one that doesn't)
- The heatsink is not covered in dust
