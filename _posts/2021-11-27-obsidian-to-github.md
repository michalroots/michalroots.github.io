---
layout: post
title: Publish from Obsidian to Github
description: Creating a Jekyll website in Obsidian for frictionless publishing on Github
summary: Creating a Jekyll website in Obsidian for frictionless publishing on Github
tags: [documentation]
---

Objective: 

**Create and edit a Jekyll website in Obsidian. Publish to Github without friction.**

(Disclaimer: I don't know how to code)

## Installing Jekyll on MacOS Mojave
It was a pain in the ass, but it worked eventually.

I needed:
- <a href="https://macpaw.com/how-to/use-terminal-on-mac " target="_blank">Basic knowledge of Mac Terminal</a>
- Read through the official <a href="https://jekyllrb.com/docs/installation/macos/" target="_blank">installation guide from Jekyll</a>
- And another <a href="https://www.awesomeinc.org/tutorials/jekyll-basics/" target="_blank">simpler guide</a>
- Finally, spent a long time troubleshooting errors I couldn't understand. Here's <a href="https://www.chadduffey.com/2021/03/Jekyll-Poop.html" target="_blank">the most succint solution</a> that worked for me. Note: I had to run `bundle update` *before* and *after* other commands. No idea why, but it works now.

### To preview the website locally:
- launch terminal and navigate to the folder with the site using  `cd ~/PATHTOFOLDER`
- serve jekyll with `Bundle exec jekyll serve`
- open <a href="http://localhost:4000" target="_blank">http://localhost:4000</a> in your browser 

## Uploading Code to Github

TBC