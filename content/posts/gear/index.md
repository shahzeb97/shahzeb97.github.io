---
date: '2022-11-15'
draft: false
title: Gear Toy
ArticleQuote: "You spin me right 'round, baby, right 'round. - Dead or Alive"
# weight: 1
# aliases: ["/first"]
tags: [programming, projects, godot]
categories: [Projects]
author: "Shahzeb Mirza"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
hidemeta: false
comments: false
description: "A procedurally generated gear fidget toy made with the Godot game engine - hand-coded mesh generation with GDScript!"
summary: A Simple Fidget Toy in Godot
disableHLJS: true # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
card:
  image: "gear.webp"
  hidden: false
# cover:
#   image: "gear.webp" # image path/url
#   alt: "Gear Fidget Toy"
#   hidden: false

#     alt: "<alt text>" # alt text
#     caption: "<text>" # display caption under cover
#     relative: false # when using page bundles set this to true
#     hidden: true # only hide on current single page
# editPost:
#     URL: "https://github.com/<path_to_repo>/content"
#     Text: "Suggest Changes" # edit text
#     appendFilePath: true # to append file path to Edit link
---

> You spin me right 'round, baby, right 'round

-[Dead or Alive](https://www.youtube.com/watch?v=PGNiXGX2nLU)


# Just Show Me
{{< figure
  src="gear.webp"
  alt="Gear Fidget Toy"
  caption="A Procedurally Generated Gear Fidget Toy made with Godot"
  align="center"
>}}

{{< video src="gear.mp4" width="50%" autoplay="true" loop="true" muted="true" caption="A demo of the gear fidget toy in action.">}}

# The Concept

As a side project to my research, I've been experimenting with the [Godot](https://godotengine.org/) game engine. 
A concept I've been playing around with was of a procedurally generated gear. 
I thought it would be a fun, highly mechanically-oriented, and aesthetically pleasing toy to make. 
It would also teach me about the engine, and in the end I would have some components that could be used in other projects.

# The Math

The unique thing about this app is that I hand-coded the mesh which describes the gear. 
I tried looking for code like this on the internet but couldn't find any that fit well with what I wanted, so I made it myself in a few days in [GDScript](https://docs.godotengine.org/en/stable/getting_started/scripting/gdscript/gdscript_basics.html). 

Gears are an extremely elegant piece of machinery, I highly recommend reading about them if you're interested. 
The mathematics behind the profile of the teeth has a long and illustrious history, with figures like Leonard Euler describing the involute shape we see commonly today.

As a crash course, spur gears like the one seen above are defined by 4 basic parameters:

1. The number of teeth.

2. The pitch, which is the number of teeth per unit length of the circumference of the gear.

3. The pressure angle, which is complicated. 

4. The thickness.

These parameters are more useful than some intuitive ones like "diameter" and "tooth height". This is because two gears of the same pressure angle and pitch will always mesh (assuming the teeth don't interfere). So if you're an engineer looking to buy gears from a catalog, directly comparing pitch is a lot more useful than comparing diameters and tooth heights and widths and working backwards.

It should be noted that the "pitch" is an imperial product. Countries on the metric system use the "module" instead, which is essentially just the inverse of the pitch, but it works the same. 

Most machine-design handbooks will have more information on this, here is the one I refer to:

*Spektor, Michael B.. (2018). Machine Design Elements and Assemblies. Industrial Press.*

# Next Steps

There are several ways forward I want to go with this project:

1. Add a button to change the texture of the gear, and maybe the background. Fidget toys should be customizable, after all.

2. When you model every triangle by hand, you get a **lot** of control over the mesh. Random bugs I found produced hyperbolic gears, spherical hears, helical gears (not in the way you think), etc. This would be a fun exercise to play with

3. I've always wanted to make an "agar.io" type game. Maybe something with a gear that absorbs other gears and adds them to its chain...

# The Code

I'm considering uploading this to the Android Play Store, so I'll be sure to post a link here when I do. Friends on iOS, I'm sorry, but I don't have a Mac to test on.

In the meantime, here is a demo on the web for everyone to play with on [Itch](https://shahzeb97.itch.io/gear-fidget-toy).

And here is the source code on [GitHub](https://github.com/shahzeb97/Gear-Fidget-Toy)!