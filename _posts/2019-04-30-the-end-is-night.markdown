---
layout: post
title:  "The end is nigh and so is the PCB and reporting!"
date:   2019-04-30 11:10:00 +0200
categories: blinds
---

# Starting to wrap things up

Hey once more before the summary documentation!

Last so on the topic on last week's agenda:
* We managed to get the softwared finally working for the presentation! After lots of troubleshooting and trial and error it seems we had trouble with not using a common ground for all of our groundings but instead different grounds with different values. So our code was working as intended, just our electrical engineering skills were "malfunctioning". This is something we could have figured out early by discussing it with someone with actual knowledge about electrical engineering, but it feels good to actually figure something out by yourself so it's not too bad we had to fight a bit with it. Bummer about the lost time though.

* We didn't have time to build a new mechanism and it turns out that we didn't! Through power of recycling we used the small clips that we have on top of the blinds window frame to attach the blinds from them. It turned out they were a perfect fit for prototyping and we saved material by not throwing them away. They are MDF though so it's not likely they're a lasting solution, but this is something we can figure out outside of the course when we have more time on our hands.

* We didn't have time to fully design and print he PCB for the presentation. This is something we aim to do before finishing the course this week. We did a bit of prototyping on our DC to DC converter in EAGLE, now we just need to route it and make another shield to replace our breadboard which we will stack using header pins.

![DC to DC converter board view](/assets/servo-shield-board-WIP.png)
![DC to DC converter logic view](/assets/servo-shield-schema-WIP.png)

* Casing is again something we won't have enough time during the course to finalise the 3D printed design for, so instead we'll keep the MDF casing since it seems to be working just fine. This is something we intend to design outside of the course when we have PCB printed and we have prototyped a bit with wifi modules to figure out most efficient 3D form for our casing.

So, about the presentation: it went surprisingly well. Half-jokingly, we brought out the fire blanket but we had a small case of short circuit during the prototyping which included smoke (not fire though!) so it was there just in case that small chance of something going catastrophically wrong. We were happy that it went well though. We could have done better powerpoint presentation with more informative sliders but otherwise it was good in our opinion.

# What's next?

* Finish the PCB design for DC to DC converter and print it
* Finish the PCB design for breadboard replacement and print it
* Clear up the blinds repository in github and include a readme explaining all the items in that repo
* Write summary documentation

Thanks for hanging us so far, please bear a bit longer!

---


##### <a href="{{ site.github.repository_url }}/tree/master/{{ page.relative_path }}">Edit this page</a>
