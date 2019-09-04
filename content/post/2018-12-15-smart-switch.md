---
title: Smart Switch
date: 2018-12-15
tags: ["lifx", "smart", "lights"]
---

![alt text](/img/post_images/181215_prototype_switch.png "Prototype smart switch")
<br/>
I quite like gadgets. So it should come as little surprise that I have been drawn by the bright future promised by smart bulbs. By their nature, in order to retain access to their smart functionality they need to be 'on' even if they are not shining. This presents a problem when faced with several decades of habit of flicking the power switch when you walk in to and out of a room.

Being 'smart' you can voice control them using Alexa, but that has some faintly annoying lag and that is even if she understands you the first time. Plus, shouting "you damn well know what I meant, Alexa!" to turn off the bedside light can be disruptive to one's sleeping partner.

So this is about the start of my quest to find another way.

<!--more-->

The smart bulb ecosystem that we have bought in to is LIFX (https://uk.lifx.com/) which I am not entirely sure how you are supposed to pronounce. Is it "life-ex" or is it "lie eff ex"? Anyway, I chose these over the main smart bulb incumbant (Philips HUE) as they reportedly have better colour reproduction from their RGB LEDs and the bulbs are brighter.

Unlike the HUE bulbs, which use a zigbee mesh network, the LIFX bulbs all connect to your WIFI and they are individually addressable using their IP and MAC address. They have an app that you can do all sorts of fun things with, like set schedules and colour schemes. One of the schedules that I have set up is to mimic the sun's cycle. That means that over the course of the afternoon they get a redder tint and then start dimming around bed time. The idea is that is good for sleep 'hygiene' by removing bright blue lights from the equation. In the morning the reverse happens, with a dim blueish light coming on and then ramping up the brightness over about half an hour. This, in combination with a fairly regular wake up routine means that I generally don't set a brash alarm as I like the 'sunrise' gently bring me to conciousness.

This brings us to the main problem. The funky scheduling requires that the bulbs are powered on in order to have the scheduled instructions delivered to them. So they can't be switched off at the main wall switch. The problem is mitigated a little by the liberally sprinkled Echos around the house, but there are issues there that I mentioned earlier, plus it can be awkward where groupings of lights are concerned.

What I need is a button of some kind that I can 'pair' with the bulbs and can toggle the shining or not shining state so that they come on at whatever setting the schedule stipulates. 

Unfortunately there isn't any first party offerings for the LIFX ecosystem (unlike the HUE which has lots). There are some third party offerings such as the FLIC (https://flic.io/) or the Logitech POP (https://www.logitech.com/en-gb/product/pop-smart-button), but the reviews of these suggest some annoying problems of their own such as lag or the need to pair with your phone. The final nail in their coffin however is the cost with the POP for example costing around £35 for a switch! Albeit at full price.

So that brings us to the tangle of wires that is shown in the picture above. Having played around with the PixelBots (https://goparker.com/post/2018-06-28-smilers-mate/) a bit, I have built up some confidence with Arduino type projects. The combination of soldering and programming is quite fun, and having a real problem to solve can be quite motivating. Thus it was that I started a Google campaign to see what other people had tried in this area.

I knew that the ESP 8266 was a little programmable WIFI enabled board that could be programmed using the Arduino IDE as Rob had been using it to make his PixelBots talk to the internet (https://www.robmiles.com/journal/2016/11/29/esp8266). 

Then I can across this (https://www.instructables.com/id/Tiny-ESP8266-Dash-Button-Re-Configurable/) which is a project that uses an ESP 01 (a teeny tiny 8226 board) to provide Amazon Dash button like functionality. Basically you can press the button and trigger a web based action such as through If This Then That (https://ifttt.com/). I am using this as the basis for my own button. The project is quite neat in that it has a configuration mode and a normal mode.

In the configuration mode you can connect directly to the button as a WIFI access point and then navigate to its little embedded web server and use the html form to enter the details you need such as your WIFI's SSID and password so that I can become part of your network.

Then you can switch to normal mode. In normal mode the board will sit in deep sleep (using little power) until you press the button. Then it will wake up, connect to your WIFI and then sent the web post. In the case of my test I sent a message to IFTTT which triggered a tweet.

I could use the IFTTT method to control the lights too, but one of the things that I want to keep to a minimum is reliance on of server infrastructure (what happens if the go bust?) and internet round trips which introduce lag. LIFX have a LAN protocol (https://lan.developer.lifx.com/) which allows you to communicate directly with the lights over your home network which deals with both the lag issue and the reliance on third parties.

You may notice that the documentation at that site is... not for the faint of heart. That is not to say that it is poorly documented, just that it requires a level of expertise that I wouldn't describe as beginner level exactly. So I returned to Google to see if I could find some examples that would help me.

And I did (https://community.lifx.com/t/sending-lan-packet-using-arduino/1460/4). This example included some code for an Arduino to talk to a LIFX bulb and find out whether it was on or off. I combined it with the other project for the button and modifed the code to allow me to toggle the on/off status of the targetted light.

And it works!

At the moment my prototype is hardcoded up the wazzoo so it only turns on and off my desk light and targetting another light involves recompiling and reflashing the button. This is not ideal. There is also some lag in pressing the button and the light toggling; around 2 seconds worth which is also a little on the long side. I am hoping that part of the lag may be caused by the liberal sprinkling of Serial.println that I included when I was trying to figure out what was going on. It may be unavoidable however as there is a small delay as the device wakes up and connects to the network. There is likely also a delay as the button first asks what the state of the bulb is, and then acts based on the result. This involves waiting for the bulb to respond to the first request.

So the next step for the button project is to integrate the configurable part of the Dash button project so that I can have the button enter 'configuration' mode setup the WIFI and give the MAC address of the light that I want to control. Ideally this would allow me to specify multiply bulbs as my kitchen, for example, has multiple downlights and I don't want to have to switch them off individually. If I can also but down the lag that would be great.

After that, when the code is stable and complete for what I want it to do, I will have a look at turning the bundle of wires in to a more compact and neat package. Then I can design and print a case for it that can be placed in the various locations in the house. In terms of the electronic bits and bobs you are looking at around £5 per switch which is more palatable than the £35 for the 'proper' one.

When I reach that stage, I will share all the parts lists and code etc.


