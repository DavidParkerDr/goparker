---
title: The Printer
date: 2018-07-05
tags: ["3d printer"]
---
![alt text](/img/post_images/180705_my_printer.png "My 3D Printer")

I have mentioned my 3d printer a few times on the blog now and I have been meaning to document the various modifications and the overall journey that I have taken with it.

So here it is.

<!--more-->

Just over a year ago, at one of the Three Thing Game events, we had a guest speaker come and give a talk about using Monogame and Unity with the Fizzyo framework. He had recently bought a 3d printer (though hadn't assembled it yet) and he was telling me all about it and how good value it was. The printer in question is the Anet A8 from available from Gearbest. It is currently priced at around £150, but a year ago I paid £124.25, which I assume is exchange rate related as it comes from China.

That is a cheap printer. Obviously it is not nothing, but it is almost little enough that if it did all turn out to be a fad for me then I could just write it off as a bit of fun that ran its course.

I did some research before taking the plunge, and there was plenty of anecdotal evidence on the internet that it was a pretty capable little machine and certainly enough to dip your toe in to the 3d printing scene and see what you thought of it. There was also a vibrant Facebook community supporting beginners with the machine and exploring various upgrade paths that are available for improving the printing quality and working of the machine.

![alt text](/img/post_images/180705_boring_beige.png "Out of the box")

Amongst the glowing reports, there was also a vocal group of people saying that you essentially get what you pay for (i.e. cheap tat) and that you should buy something better. Of particular worry were claims of it being a fire hazard due to all of the electrics running through the main board.

In fact, the first upgrade for this printer is suggested as mandatory (before even turning it on) and that is the introduction of Mosfet boards between the main board and the heating elements. The idea is that the main board controls when to activate the heated elements (the buildplate and the hot end) but all the heavy current lifting is handled by the mosfets, bypassing the main board. This substantially reduces the risk of the mainboard catching fire; a good thing.

It was also recommended that you upgrade the power supply, which I did.

Those are the essential upgrades, which is a little over £20s worth, but there is loads more that you can do. It was my observation that the primary purpose of a 3d printer is to print parts for your 3d printer, and it certainly was the case in the early stages.

I printed cable chains to provide some strain relief on the cables that connected to moving parts (these are gone now). I printed belt tensioners to enable me to tighten the drive belts that can stretch and loosen over time leading to less accurate prints. Then there are bed leveling aides. This started off with thumb wheels to make it easier to adjust it, then I added an automatic bed levelling sensor.

The sensor allows the printer to calibrate itself by measuring the bed height in 9 different places and then creating a transformation matrix allowing it to compensate for any differences in level across the bed, as long as the bed is more or less level to start with.

Once I had that I transitioned to fixed bed level. That is, instead of adjusting the corners of the bed height, all four are fixed at the same height, allowing the auto bed level to compensate for any of the small differences. That makes it a bit easier to use.

I also added a glass plate to the bed. The bed of the printer is heated (usually to around 60 degrees C) to help the print to stick to it. In the base printer kit for the Anet A8, this is an aluminium plate with a pcb heater fused to the bottom of it. Typically you would put masking tape on the build area so that you can easily remove the print after it is finished without damaging the plate or the print. 

The idea of the glass plate is that you don't need the masking tape any more and the side of the print that connects with the build plate is super smooth and shiny. In practice, I find that there can be some adhesion problems if you just use the glass plate and sometimes the corners of the printer can start to peel up. What fixes that problem pretty well is the humble Pritt stick (other glue stick brands exist). A smear of that on the glass plate before printing and the sticking problems pretty much go away. You don't have to reapply every print either. A downside to this is that it does mark the side of the print that is attached to the bed.

Another part of the original that was replaced was the cooling duct. This part blows on the print surface directed at just after the plastic comes out of the hot nozzle. The idea is to solidify it as soon as possible to help avoiding it drooping on overhangs and to avoid 'stringing' between gaps. There are a number of different designs out there claiming awesomeness, and I wasn't very scientific about it.

The only other parts I added were a couple of bits that I designed and printed myself. The first was a case to hold the mainboard and the mosfets to tidy it up a little. and the second was a mounting box for the new power supply that also included a kettle style connector and switch to allow me to more easily turn it on and off without needing to unplug it from the wall.

![alt text](/img/post_images/180705_pretty_in_pink.png "Pretty in pink")

Still with me? So I lied about the bit where I said the only other parts...

One of the cost savings with the Anet A8 is that the frame is made of a shiny black acrylic plastic. It definitely does the job, but has some limitations. One of these is that it is no 100% rigid, and the wobble as the printer throws its mass around can affect the quality of the prints. That can be countered by telling the printer to move more slowly, but then you are trading off against how long it takes to print anything.

And be under no illusions. It takes a long time to 3d print stuff.

So things that make the printer more rigid, help you to speed up the prints, and there are numerous options out there. Some people have designed braces for the frame to limit its ability to wobble and I did try some of these and they seemed to work fine.

However, I was enticed by something even cooler...

Some enterprising soul had designed a collection of printed parts that allowed you to replace the acrylic frame altogether with aluminium extrusions. They call it the AM8. 

Still not done. Well, nearly, but not quite.

A compounding factor with the frame's rigidity is that amount of moving mass. The more 'weight' that you are throwing about, the more energy is transmitted in to the frame making it wobble. So if you can also reduce the amount of mass that is moving around, then you improve the situation again and can go faster.

The Anet A8, as it comes out of the box uses a direct drive system for controlling the flow of filament through the hot end. The way it does this is with a little toothed cog which grips the filament and pulls it, forcing it through the hot end, which melts it. With a direct drive, the extruder is mounted very close to the hot end and it is powered by a chunky stepper motor. Since the hotend is one of the principle moving parts this can present a problem.

The solution is to convert it to a Bowden extruder setup. In this configuration, the hotend is separated from the extruder (which will typically be statically mounted to the frame). The filament is then pushed through a non-stick ptfe tube to the hot end. There are some pros and cons to each of the setups and one of the weaknesses of the Bowden configuration is that it can be problematic with flexible filament types. For now at least, I am not very interested in that, so if I can get my basic PLA printing faster then I am in.

I did attempt to resuse the extruder parts from the direct drive, in order to keep the cost down, but for reasons that I never got to the bottom of I never got it reliably working. So I paid my way out by buying an E3D Titan extruder. This was pricey at around £62 pounds (half the price of the original printer), but it works very well and I was a bit fed up with it at that point. 

I also needed a new hot end and I had read very nice things about the E3D-V6 hotend. I had also read that a clone of it could be had for substantially less money than an original. So having nearly choked on the cost of the Titan, I decided that I would go clone on this part for around £8 instead of around £50.

Using these parts required more printed bits as the x axis carriage needed to be replaced to hold everything.

Now we are done I think. Though I am very interested in replacing the glass bed topping with a magnetically attached spring steel build tak surface. The idea with this is that it hold very firmly to the base, but once the print is finished you just lift the spring steel plate (which is only held on by magnets remember) and just bend it, popping off your print. This is to reduce the downtime between prints whilst you wait for it to cool down enough to remove it. This is a pretty expensive upgrade at around £100 so I think I will leave it for now.

In preparing for this post I went back through my email archives to find all the purchase records for all of the different parts that I bought. I did this because although I remembered how much I paid for the original printer, I only had an estimated total of around £300 pounds spent including the upgrades. So I thought that it was time to change that estimate in to an actual figure.

The answer to that question is that it depends :). I took the original figure of everything I had bought that was 3d printer related, then I went "eek! that was way more than my estimate", then I divided the categories into actual printer parts, tools that I bought for it, pla filament, and a sort of wasted category. The last category is for parts that I bought that turned out to be the wrong size, or not work as well as I had hoped and so ended up not using them. More on this later.

So the headline total for all printer related things is £555 (and change).

Obviously, that is quite a lot more than the £300 estimate that I made previously which is a bit scary, so let's try and get it down a bit.

If you extract the tools I bought (a set of vernier calipers and a crimping tool) then that takes £22.98 from the total. A small step in the right direction. I think that it is reasonable to take this off the total as they are useful outside of the printer use case.

Next, the wasted category. For assembling the AM8 aluminium frame upgrade, I bought some so-called hammer t-nuts. The idea is that they are small enough in one dimension to insert in to the slot of the aluminium extrusions and then be rotated in to place. Unfortunately, the ones I bought were for a larger size of extrusion and so did not fit. I also ordered some Drylin linear bearings. These theoretically replace the captured ball-bearing races and are much quiter in their operation. I ran in to a bit of a problem with these as unless the tolerances are exactly right, then they can jam. I played around with them for ages, but ultimately abandoned them. I feel ok with removing these from the total as technically I could resell at least the t-nuts (though I am keeping them incase of a future project) and in any case if you want a total for just the printer as is then you don't need to include the parts that aren't in it. That brings the total done by another £47.45.

Next is the PLA filament category. This one is a bit of a 'sort-of' category. I say that because some of the filament has been used for parts for the printer, particularly for the AM8 upgrade, whilst some has been used for non-printer things. Just to muddy the waters, there are also some printer parts that I printed and ultimately abandoned, and also some failed prints where the filament is essentially wasted. So here I have the total cost of all the filament that I have purchased (including the spool that is arriving today): £117.78.

That is 6 spools of filament of varying colours. I have also tried different price points for the filament ranging for expensive £30.09 for 750g to cheap at £13.99 for 1kg. I think that the expensive one is not necessary and generally at the moment I am just trying to source the cheapest. At some point I would like to do some experimenting as I did have some complications with the very cheapest, but I wasn't paying a great deal of attention to 'dialling it in'.

So that brings the just printer and parts total down to £367.13, which is considerably closer to the ~£300 that I estimated. To account for the aforementioned printed parts cost, you probably want to add a spool's worth. So let's say around £385 in total.

So, part of the reason that I wrote this post is that I have been meaning to do it for a while to have some kind of referable record of what I did. The reason I finally did it is that a friend of mine was considering getting a 3d printer himself so I thought that this would kill a couple of birds with one stone and provide him with some information that he may find useful. Obviously, this was fairly high level (despite the length), but provides a starting point for asking questions, which I am more than happy to answer. I may also expand on some of the parts at some point in the future as the need arises.

This brings me back to a question that was kind of hinted at above by the internet posts about spending your money on buying a better printer in the first place, rather than going through this hackedy upgrade process. The question is, should I have done that?

I have kind of mixed feelings about that. I don't regret it at all. I have learned a great deal from assembling the kit, disassembling it, upgrading it, and using it. It was easier to swing a gradual drip feed of costs than a chunky up front cost.

Here comes the however. If I wanted another 3d printer, would I replicate what I have now (skipping the trial and error obviously)? I am not sure. For less than (or up to, depending on the source) the £385, that I concluded above was the notional cost of the printer as it stands now, you could purchase a Creality cr-10. This has an aluminium frame already. It also features a larger build volume meaning that you can print bigger things. It is also fairly well regarded it appears.

There is also the option of going even more DIY than the kit I started with. There are designs out there such as the Hypercube Evolution (https://www.thingiverse.com/thing:2254103) which uses the core-xy model (moving the build plate up and down in the z axis, instead of forward and backward in the y axis like my printer. I would strongly consider doing this.

I guess that it would come down to a budgetary decision in the end. I think that if I had £700, then I would consider getting a Prusa MK3. This is a very highly regarded printer with a number of component and software improvements over what I have now.

But would I spend that much to replace my current printer? No? He says uncertainly. There are just too many gadgets and I am not independently wealthy, more's the pity.

The end.

P.S. Below is just a list of all the things I priced up above, mostly for my own memory.

15/6/17 Anet A8 £124.25 gearbest  
20/6/17 Bed sensor £8.63 gearbest  
15/6/17 Mosfets x 2 £9.38 ebay  
22/6/17 Glass bed £14.99 ebay  
30/7/17 Drylin bearings £13.85 ebay  
1/8/2017 E3D-v6 clone £8.46 gearbest  
7/9/17 E3D Titan £62.61 e3d  
15/6/17 360W PSU £13.85 ebay  
15/6/17 100 x cable crimp ends for m4 bolts £3.19 ebay  
16/6/17 power socket with switch £0.99 ebay  
16/6/17 3d filaprint pink £20.95 ebay  
20/6/17 crimping tool £7.99 ebay  
25/6/2017 gt2 timing belt 5m £3.42 ebay  
26/6/17 100 m3 hex nuts £1.99 screwfix  
16/7/17 innofil3d black pla £30.09 amazon  
25/7/17 digital vernier caliper £14.99 amazon  
29/7/17 AM8 aluminium parts £56.21 motedis  
30/7/17 20x aluminium l shape brace £6.56 ebay  
30/7/17 nuts and bolts for AM8 £16.43 orbital fasteners  
30/7/17 10 x rubber feet £3.40 amazon  
5/8/17 aluminium hammer T nuts £33.60 ebay (don't fit!)  
10/8/17 m5 t nuts £27.50 ebay  
26/8/17 pla grey £20.95 ebay  
5/9/17 nuts and bolts and washers £5.27 screwfix (not sure what for)   
28/2/18 primavalue pla dark grey £15.90 amazon  
10/5/18 sunlu 3d pla plus salmon orange £13.99 amazon  
4/7/18 primavalue pla green £15.90 amazon  
