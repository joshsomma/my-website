---
title: Tips for 3D Printing N00bs
layout: post
keywords:
    - 3D printing
    - Anet A8
    - DIY
author: Josh
---
... from a 3D printing n00b.

I've spent a good number of hours now working and learning on my Anet A8 3d printer. The printer was given to me by a former colleague intact but not functioning properly. I let the printer sit on the floor of my garage for a good 8-12 months before I finally cleared a space on the workbench in preparation of figuring out how to get it to work.

To say I had a lot of problems getting the printer to work properly is an understatement. There was a lot of Murphy's law going on where if something bad could happen it did. I physically broke parts of the machine, I bricked the main board firmware, I had electrical faults that could have been fire hazards that I needed to repair. The list goes on, disaster after disaster. I would say to anyone interested in these cheap 3d printer kits to prepare yourself for a lot of work.

But I persevered and finally, finally have the machine in good working order and also feel like I have learned the core knowledge required for basic FDM 3D printing using PLA and PETG. I'm far from an expert but I've learned a lot of lessons so I'd like to share with you dear reader a few random tidbits of advice I learned the hard way....

**Try to control ambient temperatures**

Given that the temperature of both your hotend and bed are crucial to successful printing, being able to control the ambient temperature in the space where your printer is located is pretty important. My printer is in the garage which is very drafty. The temperature in the garage largely depends on the temperature outside and this as you know can vary widely in a place like London. In cold conditions, I pretty much can't print at all in the garage.

Since the ambient temperature in my printing space varies this means to some extent I have to vary my hotend and bed temperatures as well.  Being able to maintain consistent ambient environmental conditions removes the need for making these tweaks. Having a space to operate your printer with a stable environment gives you a consistent baseline for the temperatures of your hotend and bed.

**Be really careful during firmware updates**

I was flashing my firmware and the IDE I was using to transfer the config files from my computer to the printer was hanging. I made the mistake of switching off the machine while the process was still running. Maybe I had no choice and the process would have hung forever anyway but shutting off the machine mid-flash bricked the mainboard on the printer. Disaster. Fortunately I have an Arduino Uno and that can be used to restore the bootloader on the printer mainboard but it was painful. Thanks to a [very helpful video](https://www.youtube.com/watch?v=RQIizXtf9oo) from Daniel at Crosslink I was able to get the information I needed fairly quickly. However, fixing the issue required wiring the Arduino directly to the printer mainboard. So to sum, don't do what I did. :)

**Cleaning the hotend nozzle**

Q-tips work well for cleaning the hot end nozzle between prints. The Q-tips are able to grab the oozing plastic very effectively. However, Q-tips are not environmentally friendly (sustainability of 3D printing in general is a topic for another post) so I've switched to using paper towels that have been sprayed with an alcohol solution. This is less convenient as you have to be careful about burning yourself on the hotend but the result is good. I mix 25% rubbing alcohol to 75% water in a spray bottle for the solution.

Also, I often remove the fan vent to clean the nozzle and forget to put it back on when I start the next print. Remember to put the fan vent back on (facepalm). It drives me nuts when I do that.

**Read the readme file**

I download most of my stl files from Thingiverse and there is a readme file included in the zip file. I'd suggest always reading the file as you may find a lot of good information relating to your slicer settings.

**Consider the orientation of your print on the bed**

I print on a glass bed and use binder clips to hold the bed to the stock aluminium bed. I've had lots of prints fail because I didn't think about the orientation of the hot end assembly and in particular my inductive sensor. My setup has my sensor in front and to the left of the hot end. There's been a number of times where my sensor has crashed into the clips causing the print to fail because I didn't think about the orientation of the model on the bed vs where the clips are located. Remember when laying out your model in the slicer to think about where an obstruction (like a binder clip) might be located.

**Easy automation**

I use a smart plug on the outlet where I keep the printer plugged in. I can turn the printer on and off remotely (remember it's out in the garage) which gets the Octoprint server up and running without needing to go outside. Then, using Octoprint, I can preheat the printer before I go out to start the printer (you should generally let the printer heat up for ten minutes to let the metal expand). Finally, if I leave the garage while the printer is running, I can turn off the printer remotely when the print is finished, which I can confirm using the webcam through Octoprint.

**To sum up...**

So there you go... a few easy, n00bish tips I've learned on the way. I hope they can help you avoid some of the pitfalls I've fallen into while learning how to operate my Anet A8. Thanks for reading!



