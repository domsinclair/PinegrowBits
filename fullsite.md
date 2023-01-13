# Full Site Pinegrow Build- [Full Site Pinegrow Build](#full-site-pinegrow-build)

- [Full Site Pinegrow Build- Full Site Pinegrow Build](#full-site-pinegrow-build--full-site-pinegrow-build)
  - [Objectives](#objectives)
  - [Getting started](#getting-started)
    - [WordPress settings](#wordpress-settings)
    - [Colours and Fonts](#colours-and-fonts)
    - [Site layout](#site-layout)
    - [Connect to GitHub](#connect-to-github)
  - [A natural break](#a-natural-break)

This tutorial marks the first of a series where we'll embark upon a full site build of a WordPress site. It will not be a masterpiece of visual design but it will explore how we can integrate both the desktop and plugin versions of Pinegrow.

In addition to that we'll be looking at ways to minimise reliance on additional plugins.

It seemed a sensible idea to work on something of my own for this series on the grounds that it's work I'd planed to do anyway.

## Objectives

1. To put Pinegrow through it's paces and to establish, or at least to get some understanding of the best / most efficient way to get both the Desktop and plugin versions working side by side.
2. I want a site that will be Dark Mode enabled from the outset. My own preference, largely age related I suspected as my own eyes get older, is for dark themes.
3. I want to try and make the site as accessible as possible from the outset. This area of site development is fast becoming a minefield so working out some efficient ways of tackling it will be useful.
4. I want the site to work in parallel with another one of mine, possibly going as far as highlighting some content from it. Exploring how this might be done effectively could be interesting.
5. I'm not a natural designer, although I instinctively know what I like, so it will be interesting to explore resources that help achieve at least some semblance of a clean design.
6. The site is going to be WordPress based, as is the one I want to tie up with as it happens. I would very much like to reduce the reliance on plugins to do things that either Pinegrow does itself or which, in truth can be done just as efficiently with some additional code. Pinegrow's integration with VSCode should make this side of things much easier.

## Getting started

I'm going to start this off in VSCode , linked from the outset to a Private repository on Github. The hosting provider I use supports Git and GitHub so That will already bake in some form of backup protection for the inevitable mistakes that I'm likely to make.

For the ske of speed I'll use Local to host the development site. My Hosting provider has dedicated WordPress packages that come with automatic staging and I have a good fast rock steady internet feed so I could just work off site from the outset but not everyone has those advantages so it makes sense to work locally.

The local site will be configured to use Apache, My Sql 5.8 and one version below the current PHP release (at the time of writing this equates to PHP v8.1).

I've decided to use TailwindCSS as its free, integrates beautifully with Pinegrow and supports DarkMode pretty much straight out of the box which immediately ticks off one of my objectives.

The basic setup procedures have been covered here before so for now we'll just say that you'll want to set up your own local wordpress site. You'll also want to setup a working folder in VSCode in which to create you basic Tailwind site. Once you've done that you can fire up Pinegrow and create a new project based on your new site.

### WordPress settings

One of the overall objectives for the site is to make it as fast as possible. One of the most common factors for slowing down a site is the size of the images that get displayed. To be really efficient your site's images need to be optimised.

I'm going to adopt a two pronged approach to achieving this. Firstly I'm going to load the [Short Pixel Image Optimisation plugin](https://shortpixel.com/products/shortpixel-image-optimizer) to the local site and configure it. I have a Short Pixel account with a fair dollop of credits attached to it hence my choice. I'll also whilst I think about it uncheck the Organise my uploads into month and year based folders in the WordPress Media settings.

I'll choose the options in Short Pixel to create webP images and to convert png images to jpeg where possible.

Within Pinegrow itself well be making use of the picture tag to display our images.

I'm also going to want support for svg's. WordPress prevents the automatic loading of SVG files by default because of the potential security threat that they can pose. You can add a short block of code to the back end of the site to change this default behaviour or you can do so with a plugin. The plugin options for this functionality will generally perform a sanitisation check on the uploaded svg files and given that these plugins have little or no impact on site performance then we may as well use one. [SvgSupport](https://wordpress.org/plugins/svg-support/) is my own goto plugin for this job.

### Colours and Fonts

If you already have a set of strong brand colours and fonts then this is a relatively easy thing to decide on, it's not so easy when you don't. This fact in and of itself might be a good argument for using bootstrap instead as there are a wealth of themes and blocks that can be used to put something together that looks reasonably good.

One resource that i have come across that I have really enjoyed reading is [Refactoring UI](https://www.refactoringui.com/?ref=resources) which looks at designing interfaces from a developer's point of view. This is one of the very few works on design that has actually made any sense to me and is another reason for opting for Tailwind.

The book talks about both colour and typography. We can customise these aspects of Tailwind very easily from within Pinegrow so rather than discuss this further we'll tackle it when we have need to.

### Site layout

My first attempt at creating this site was done almost two years ago using Oxyen with a very hefty reliance on an Oxygen Add in, OxyNinja. It's not something that I'm overly happy with now so it makes sense to change it.

Initially I'm going to go with a front page that introduces some of the things that Vtl Software does. Buttons in the descriptive sections on the page will link to individual pages that go into more detail. I'll also add a header and Footer.

The other site I want to link up to is more tightly focused on Education. I'm not sure if this will work or not yet but assuming that it can be made to work then we'll make space for it on the front page as well.

I'd like the site to be simple, clean and informative.

### Connect to GitHub

Lastly, and before we go any further this is the time to make the first commit to GitHub. I'm going to assume for the purposes of this tutorial that you are familiar with Github and how it works. It's a largely free resource these days and its deep integration into both VSCode and VisualStudio have made it much much easier to use, in my opinion at least.

If you don't know about Git and the whole idea of version control then it's worth taking a break and doing some research into it. It is not purely a backup tool, it goes way deeper than that.

Not everything in your project actually needs to be included in your Git repository. Git has a file (gitignore) in which you can specify things that you don't actually want or need to track. There is an [interesting discussion on this](https://forum.pinegrow.com/t/what-should-we-include-in-our-gitignore-file/6713/5) on the Pinegrow forum.

## A natural break

This seems to be as good a place as any to break. we have a set of objectives in mind and we've created a basic tailwind based site and then gone ahead and based a new Pinegrow project on that and started work in that on creating a wordpress theme. All of the practical aspects of what we've done have been well covered already so there hasn't really been a need to go over ground that has already been well trod.
