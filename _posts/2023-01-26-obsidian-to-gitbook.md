---
layout: post
title: Publish from Obsidian to Gitbook
description: Create a gitbook, edit in obsidian.
summary: Create a gitbook, edit in obsidian.
tags: low-tech
---

Objective: 

**Create and edit a Gitbook in Obsidian. Publish without friction.**

Let's get right to it.

Create a [github](https://github.com/) account if you don't have one yet.


1. Create a new public repository on github
2. Install Gitbook app in your github account, then give it access to your repository Applications > Gitbook> repository access > REPOSITORY
3. Create a new [gitbook](https://gitbook.com) and publish.
4. Edit > synchronise with Git – choose the REPOSITORY, main branch, select writing content on gitbook (improtant) gitbook will copy content to github now
5. delete synchronisation with git, then redoit, this time selecting write on gitbook –> 
6. github sync desktop, clone repository choose REPOSITORY, then local path






Note: This process also allows to publish from Obsidian to Github, via [Github Sync](https://docs.gitbook.com/integrations/git-sync/enabling-github-sync). Create a Gitbook, sync with Github, then use Github Desktop to sync with Obsidian 🤓.

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

That was easy, because I did this before, and Github has a <a href="https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages" target="_blank">good manual on how to do it.

- I created a new repository called `<username>.github.io`
- I cloned the empty repository from Github to my computer using <a href="https://desktop.github.com/" target="_blank">Github Desktop</a> 
- I copied the contents of the website I have been editing on my computer to the github folder and pushed changes to Github.

The website is now live at heymichal.github.io, but there are still a few things to do.
	
## Editing with Obsidian
	
Open the local folder with my github page as a vault in obsidian. That was super easy. I'm now editing this post in Obsidian, then commit changes and merge via Github desktop.
	
Note that it takes some time for the changes to appear on the live site.
	
💡 I later moved the entire local folder with my site into a /web folder inside my main obsidian vault.

## Setting up Netlify
	
The next step is to fix tags not working at all on the site. I suppose it's because of some incompatibility between the template I started with and Github pages. I know that the template was using <a href="https://netlify.app" target="_blank">Netlify</a> to deploy the site, so I guess I'll do the same.

Super easy and works like a charm.
	
- I added a new site from git
- pointed to my repository with the site on git
- deployed
	
I now have a funky netlify url: `https://sleepy-mahavira-46dee4.netlify.app/` which I can change into a custom domain with SSL, which is the obvious next step.
	
I also tested the speed of publishing and it works instantly. I edit in Obsidian, push with Github Desktop and it's live.
	
The only trouble is that images don't seem to be showing at all in previews on social media (I'm using <a href="https://socialsharepreview.com/" target="_blank">this tool</a> and <a href="https://cards-dev.twitter.com/validator" target="_blank">twitter card validator</a> to test). I checked the <a href="https://milanaryal.com.np/integrating-social-meta-tags-into-jekyll/" target="_blank">YAML frontmatter</a> and it all seems fine to my eye:
	
layout: post <br>
title: The Red Caped Girl <br>
description: The magic happens when I tune into myself. <br>
image: /assets/touch-of-universe.jpg <br>
tags: [letters] <br>

and yet, I keep getting this error: 
	
`og:image can't be found at the defined URL`
	
I'll troubleshoot it later.
	
## Setting up custom domain
	
This was quite straightforward, even if the [manual](https://docs.netlify.com/domains-https/custom-domains){:target="_blank"} from Netlify was a bit overwhelming.

Set up custom domain, when you get the new DNS configuration login to your domain registrar and setup the new DNS configuration, and then wait for some time for the website to show up at the new address. It took around 2 hours in my case, and the site is now operational!
	
🎉
	
## Troubleshooting SSL Certificate
	
It turns out that while the site was live, something didn't work with the automatic SSL encryption. I went to domain settings in Netlify, clicked on "renew certificate" and less than a minute later it was working properly. 
	
## Optimising Obsidian <> Github Flow
	
For now I've been using a separate obsidian vault for my website, but actually, why not keep it all together?
	
I've created a new folder ```/web``` in my main obsidian vault and I moved the folder with website files ```heymichal.github.io``` inside.

## Is this Useful?

Well... I hope so. Personally speaking, it did change my entire experience of creating digital content.

If it seems to be making a difference for you, then I'm really happy. Enjoy!

You might also enjoy this article - [Personal Website Flow (Full Version) - How I Use This Website](https://michalkorzonek.com/personal-website-flow-full){:target="_blank"}, where I'll show you how effortless it is to fly while this setup is operational.

If you feel like supporting my work, [Patreon](https://patreon.com/michalkorzonek){:target="_blank"}  is a great opportunity.

