+++
title = "House In A Storm Demo"
date = "2024-12-30T13:15:22-05:00"
#dateFormat = "2006-01-02" # This value can be configured for per-post date formatting
author = ""
authorTwitter = "" #do not include @
cover = ""
tags = ["Game Design", "Sound Design", "Experimental"]
keywords = ["", ""]
description = "Game prototype to experiment with sound design and the effectiveness of microsoft's Project Acoustics {{<youtube L2gG9kQsaxQ>}}"
showFullContent = false
readingTime = false
hideComments = false
+++

{{<youtube L2gG9kQsaxQ>}}

# Summary

This was the culmination of some preliminary research into instilling fear using sound. This project was inspired by the findings of several papers, and foley practices in film. The concept was to simulate a dangerous environment by using sound and visuals that recalled childhood vulnerabilities, instinctual fears, and player experience/expectations of horror films. So far, this project hasn't certifiably proven anything, but still turned out to be good practical experience with Unreal Engine, metasounds, and sound design. 

# Deep Fear

The experience I wished to create in "A House in a Storm" was a deep-rooted, subconcious, unexplainable fear. The kind of feeling that takes a front seat, but defies reason. This goal inspired the setting and premise for my game. The player views this big, dark house from the perspective of a child who has been left home alone. When the power goes out, they are left in the dark in an almost familiar space. This is home, but not their home. Conceptually, the player shares their characters perspective as they are also in an unfamiliar home-like space.

> "He did not like the cellar, and he did not like going down the cellar stairs, because he always imagined there was something down there in the dark. That was silly, of course, his father said so and his mother said so and, even more important, Bill said so, but still..." - Stephen King, It

The sound systems I implemented attempt to emphasize the possibilities of something lurking in the dark, without giving the player any concrete answers. The walls creak, pipes twang, and mice scurry in the floors. Every sound is created using a metasounds system, that blends different samples togeather, making sure not a single sound is heard in the same way (or in the same place) twice. 

# Project Acoustics

I turned to Project Acoustics as a way to realistically simulate the attenuation and spatialization of my sounds. Project acoustics bakes the sound attenuation information of an area into an array, based on spatial dimensions and wall materials. The upside is that this method allows for a very fast and very accurate simulation of how sound would behave in a space. Unfortunately this baking process is very slow, and also results in a very large data file.