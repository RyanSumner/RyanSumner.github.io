---
layout: post
title: MDDN442 Project 1 Process - Time Dilation
---
Right first thing is first, I need to implement the Time Dilation equation and have something to compare it to real time.

- Clocks!

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstclocks.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstClockWorkings.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstClockHandWorkings.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstsliders.png)

The controls are there for that interactive part of the concept.

- Added rate of time slider(the speed the clocks turn)

- Added time dilation slider (controls the time dilation effect on the second clock)

- Added reset button that restarts the clocks


![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/defaultbutton.png)

- Added Default Button (sets the sliders to predetermined values, for when things get too crazy).




The Current Display:

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstDisplay.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstDisplayWorkings.png)






Around this time I was shown the RGBAdelay pre-made component which gave me the idea to work on my own version for my needs in the project.


![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/RGBAdelay.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/RGBAdelayBasis.png)
I messed around with the RGBAdelay in order to understand how it worked.

From this I created a similar effect that instead of delaying the RGB, it delayed different layers of opaqueness


![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstOpaque.png)



In the meantime I created 2 additional clocks for additional levels of the delay.

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/4clocks.png)



The Current Display:

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/secondDisplay.png)

- Added Text to the sliders to easier identification





During my tinkering with the creation of the opaqueness delay, I found that different ordering of levels and levels of opaqueness used created different effects.

There were 3 that I made:

- The real time layer was most prominent with the other layers have low opaqueness in comparison.

- All layers had the same level of opaqueness.

- The 4th layer was the most prominent (the inverse of the first effect)


![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/DiffVideoDelay.png)


It was around this time that I noticed that with 3 different caches (1 for each extra layer) per effect, it was starting to affect the FPS and memory consumption.

I found a way to solve this by using cache select, so that only 1 cache was being kept per effect and the layers were just selecting that 1 cache at a delay.

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/firstCacheSelect.png)

Now all I had to do was to link the amount of delay and the size of the cache to the relevant clocks.

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/cacheSizeChange.png)


Still being undecided about what effect to choose, I just created a slider that acted as a 3-way switch to choose what effect was to be used.

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/EffectSlider.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/EffectSliderWorkings.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/EffectsSwitch.png)





However with everything linked up, have 3 caches with increasing size tended to take up a lot of memory very quickly, making the FPS drop quite noticeably still.

So I made such that there was only 1 cache and everything else was selecting from that cache.
The side effect however was that it made the switching layout quite a maze...

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/DelaySwitchFinal.png)





Somewhere along the line I made a pause button, I thought it would be useful for stopping the application to not take up more memory, and to take not of things like the clocks.

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/PauseButton.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/PauseWorkings.png)
As part of the local component there is a time component, the button simply adjusts the 'play' parameter as a toggle button.







With most of the technical stuff out of the way, all that was left was the update the display and make things look better.

One of the criticisms I received was to be able to see the different layers separately.

Another thought was to use colours instead of words for labelling to make things simpler to look at.


The first thing to do then was to colour the clocks and their respective sliders.

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/4ColouredClocks.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/ColouredClockWorkings.png)
Note: the scaling done to the clock via the transform node is there to retain the aspect ratio in the panel there clocks are in.

Something I also added to the sliders was a moving translucent dot, I wanted to remind the user that time dilation was all about going fast.

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/4ColouredSliders.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/ColouredSliderWorkings.png)


Next was the separate layers.

I just made the coloured clocks translucent over their respected video layers.

While I was at it I thought it would be a good idea to add an hour hand to the clocks for time comparison over a longer period of time (or when the rate of time slider is turned up for a bit).

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/4TranslucentColouredClocks.png)
![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/4TranslucentColouredClocksWorkings.png)





Now for the finishing touch:

A Time Dilation Graph!

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/Graph.png)

I thought I needed something that would be educational (the original concept of this project) and would tell the user what this application was about with the need for a title.







Thus we have the finished product:

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/DisplayFinal.png)

![_config.yml]({{ site.baseurl }}/images/Time Dilation Documentation/FinalOverview.png)
