---
date: '2022-09-04'
draft: false
title: no name® Todo List App
ArticleQuote: "Good artists copy, great artists steal. - Pablo Picasso"
# weight: 1
# aliases: ["/first"]
tags: [programming, projects]
categories: [Projects]
author: "Shahzeb Mirza"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
hidemeta: false
comments: false
description: "A minimalist Flutter todo list app inspired by the no name® brand's clean aesthetic - my CS50x final project!"
summary: A Simple, Minimalist, Flutter App
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
  image: "noname.webp"
  hidden: false
# cover:
#   image: "noname.webp" # image path/url
#   alt: "no name Todo App"
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

> Good artists copy, great artists steal.

-[Pablo Picasso](https://quoteinvestigator.com/2013/03/06/artists-steal/)

# Android Development with Flutter

Over the pandemic, I finally took the time to learn how to make a mobile phone app. After reading several articles about the different ways this could be done (native development, React Native, Xamarin, etc.) I settled on using Google's fresh new (at the time at least) framework for cross-platform app development: [Flutter](https://flutter.dev/).

{{< figure src="flutter.webp" alt="Flutter Logo" align="center" >}}

Flutter is a very straight-forward, Dart-based framework that offered hot-reload, JIT compilation, and a very well-thought-out library of "widgets" that would let me beautify my app. After familiarizing myself with the basics, I wanted to make a simple app with a very distinct look.

# The no name® Appeal

I've always loved the no name® brand [identity](https://youtu.be/78feeBgCwkA). It's clean, punchy, delightfully mellow, and shockingly easy to recreate.

{{< figure src="noname.webp" alt="no name brand logo" align="center" >}}

I also loved the subtly snarky "tag lines" the marketing team put under certain products. A no name® brand water bottle might be labelled:

### water bottle
##### for drinking

With this identity in mind, and using the closest font to Helvetica I could find, I coded up a simple Android app!

# Pictures

Below are some screenshots of the app running on a real world Galaxy S6! 

{{< figure src="nonameportrait.webp" alt="Portrait Screenshot 1" caption="Portrait Mode" align="center" >}}

{{< figure src="tasks.webp" alt="Portrait Screenshot 2" align="center" >}}

{{< figure src="nonamelandscape.webp" alt="Landscape Screenshot" caption="Landscape Mode" align="center" >}}


# Videos

And here are some videos of the app in action (also taken from my old Galaxy S6)! Functionality includes making to-do items, checking and unchecking them, editing items, and deleting them ✅✅✅.

{{< video src="maketasks.mp4" caption="Making Tasks" muted="true" >}}

{{< video src="rotate.mp4" caption="Rotating the Screen" muted="true" >}}

{{< video src="edit.mp4" caption="Editing Tasks" muted="true" >}}

{{< video src="delete.mp4" caption="Deleting Tasks" muted="true" >}}

# Getting the App

This app was only made to work on Androids since I don't own a Mac to use Xcode (so ironically I can't use it on my own iPhone 🙃). Right now the only version of this that exists is a private APK in my working Flutter directory, clocking in at 5,107 KB. 

For the sake of legal safety, I never hosted this app on the Google Play Store. The app is small enough that I could host the download on this website through GitHub Pages, but I found in other testing that modern android phones didn't love downloading unregistered APKs from random websites. 

The eventual plan is to host the APK on my GitHub itself along with the whole project, so keen readers can jump through all the hoops to get it if they need. Right now, the codebase is a mess (and huge because Flutter), but I will edit this post when I do eventually put it up!

# Closing Thoughts

I learned so much by making this app, though I know I have a lot more to learn still. Fun fact, This app also served as my final project for [CS50x](https://cs50.harvard.edu/x/2022/) (a free, high-quality beginner programming course offered by Harvard which I highly recommend!). 

For simple projects, you don't really need to think about architectures (like MVC) and barely need to think about good programming practices. Although the simplicity and speed of development is nice, it really limits how much functionality you can add or if you ever want to add anyone to your team. As the old saying goes:

> Go fast alone, go far together

I hope to return to making apps again some day when I have time (maybe a simple game next time 🤔).