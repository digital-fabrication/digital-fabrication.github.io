---
layout: post
title:  "Dude, where's my electrical engineer?"
date:   2019-04-22 01:04:00 +0200
categories: blinds
---
Kept you waiting, huh?

There has been +3 weeks of silence mainly due to lazyness to report everything and because of personal matters. Apologies for all that. However, this doesn't mean we've been idling about.

Last time we were figuring out what kind of housing we were going to do for the blinds controller and waiting for the new parts. Let's continue from that.

# Making the insides tick just right and not go BOOM!

Last time we were still waiting for all the materials. We received all the ordered parts on 2nd of April. We had started prototyping the software setup with AutoCAD and simulating the system so when we got the actual parts into our hands we wouldn't immediately kill the servo or fry the development board. This is especially important since none of us has too much knowledge over electrical engineering so we were very much learning as we went on. We actually received word of warning from Fab Lab staff about our lithium polymer battery and how to not make it burst in to flames!

Currently we have simulation on AutoCAD of our breadboard with all of its components working perfectly. For some reason though, we're having some problems with the servo just going in to its max position and not listening to the data we're putting through our breadboard. We checked with a multimeter that all our connections were good and with an oscilloscope that our pulse widths are correct. We might be pushing logic on incorrect voltage through (in last attempt it was 4,7 V while it should be steady 5 V), so that's something we should test the next attempt we get.

Because servo also needs 5 V power, but we have controller that takes and will only push 3.3 V power. Therefore, we need DC to DC converter which we decided to build on our own with help from the Fab Lab staff. This was to avoid ordering any additional off-the-shelf complete products and since we had bunch of components ready for this from other projects. We did initial PCB plan for the converter in EAGLE. Before we go do the PCB printing though, we also have to get the breadboarded version to work so we can add all of its electrical components with the converter PCB design and have 1 PCB shield ready to go. We already did initial planning how we're going fit all the components on same shield. All our plans are currently on our [github](https://github.com/digital-fabrication/blinds). 

That ends the update on our electrical components. But it's not only what's on the inside that matters, sometimes you need to look at the outsides as well.

# How's the casing, Doc?

I would like to say we have solid and concrete plans for the casing, but we have mainly messed around the electrical components. We have plans to quickly decide things after current holidays.

# So many things to do, so little time...

In short, we have to:

1. Get software working correctly with the breadboard
2. Build a mechanism that connects the servo to blinds stick
3. Print PCB shield that has the converter, buttons for controlling the blinds and all necessary electrical components to get the previous to work and powered up
4. Lock down the casing design, model and fabricate it

If we have additional time, we were planning to do some calibration on the photosensors but it's likely that we won't have enough time as we're suppose to do the presentations this week...

That's all folks!

---

##### <a href="{{ site.github.repository_url }}/tree/master/{{ page.relative_path }}">Edit this page</a>

