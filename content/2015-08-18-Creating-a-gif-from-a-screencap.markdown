---
layout: post
title: "Creating a gif from a screencap"
date:  2015-08-18 00:54:00
categories: tips mplayer imagemagick gif
---
First you need to recorder you screen. In order to this you can use kazam.
After you have recorder you screen.

# step one
install imagemagick mplayer

# step two
mplayer -ao null <file-name> -vo jpeg:outdir=path-where-save

# step three
convert path-where-save/*  image.gif


After this, it's done!
