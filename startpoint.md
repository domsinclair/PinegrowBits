# WordPress Themes:  Theory and Practicality

- [WordPress Themes:  Theory and Practicality](#wordpress-themes--theory-and-practicality)
  - [Basic Requirements](#basic-requirements)
    - [WordPress](#wordpress)
    - [HTML and CSS](#html-and-css)
    - [PHP and Javascript](#php-and-javascript)
    - [A Good IDE](#a-good-ide)
  - [The WordPress Theme](#the-wordpress-theme)
    - [Theory](#theory)
    - [Practicality](#practicality)
    - [Style / CSS](#style--css)

If you're reading this having come from the tutorial on creating a basic WordPress theme then you'll already know that it's not that difficult to accomplish the task in Pinegrow but you'll no doubt be thinking that the result was hardly inspiring and not exactly practical either.

What is really required is a good basic starter theme that can be customised easily and which in due course (with the addition of some pre built Gutenberg blocks) can be used by end users to add content simply, quickly and hopefully, without breaking anything.

This tutorial is going to cover theory rather than practice.  There is a wealth of information available both on the official WordPress site and of course in a myriad of articles that can be found all over the web.  The purpose of this article is not to replicate that information but to try and distill just enough to provide a primer on what constitutes the basics for a workable WordPress theme and what ,from a practical perspective, you should be doing to create for yourself a basic starter theme that you can reuse for future projects.

If you're coming to this from a background of using WordPress page builders and themes (especially ones like Elementor and Divi) this may seem daunting.  Users of Oxygen or Bricks will have more of a head start here but there may still be aspects of this that are off putting.  In truth what we are about to discuss really isn't that difficult to understand.  All that is required is a little patience and a willingness to be open to new concepts.

One of the most common fears expressed by people thinking about moving away from page builders is that it means that they will have to write lots of code.  It's certainly true that you will have to write some code at some point.  However you'll almost certainly be doing that because you've discovered that there is something that you want to do that can only be done by putting pen to paper (in a metaphorical sense). At that stage you'll be writing code because you want to and that's when you'll discover that it's really not that frightening a thing to do.  

Without doubt once you start to get comfortable writing little bits of code then before long you'll find yourself writing entire chunks of code that actually do something and with that comes a certain satisfaction as you sit back and think to yourself 'I did that and it works, moreover I wrote it'.

## Basic Requirements

We'll take it as a given that you already have a computer and the other bits of hardware that make it possible to physically do the job. 

### WordPress

As we're discussing WordPress themes then a basic understanding of what Wordpress actually is will be helpful. Particularly useful will be a clear understanding of what WordPress was originally designed to do, specifically to provide a platform on which people could easily produce content in the form of blog posts.  That it now acts as the base for nigh on forty percent of all websites I suspect was far from the minds of the developers who first conceived of the idea.  With that of course has come one , if not its main drawback, the wealth of plugins that have been developed to accomplish specific tasks many of which in all fairness are not particularly good or written with a view to working well with other plugins.

### HTML and CSS

A basic understanding of what css and html are will be useful. In truth you probably already have a reasonable grasp of what they are.  At the very basic level html provides the structure of a website and css adds some styling to it.

### PHP and Javascript

Php and Javascript provide the glue that makes that makes the structural elements work.  Put simply you can create a button with html and css but if you want something to happen when it is clicked  (or touched) will require some php or javascript.  Whilst it is not necessarily vital to know how these languages work, knowing how and where to incorporate them is.


### A Good IDE

An IDE or Integrated Development Environment is crucial to make your work easier to complete.  If you're reading this because you're in the process of trying to learn what Pinegrow can do for you then you already have one very good IDE but to make it better still I'd suggest combining it with Visual Studio Code. 

IDE's are a matter of personal choice every developer has their favorite and it's not the purpose of this article to praise one over another.  Try out as many as you can but remember this.  At the end of the day all code is basically text and with that in mind you can do everything in Notepad.  Granted it's not exactly the most exiting environment in which to write code and it lacks all of the bells and whistles that come with professional IDE's but it still does the job.


## The WordPress Theme

### Theory

As has been said earlier WordPress started out as a Content Management System (CMS) designed to faclitate blogging.  Part of the structure that makes this possible is its use of themes.  Losely these provide the framework to;

1.  Present the content (done through a series of hierarchical templates). 
2.  Style the content via the inclusion of stylesheets.   

If you're coming to this from conventional page builders, especially the more advanced ones, then you may well be thinking at this stage that you're in familiar territory, after all Templates form a fundamental part of the way those work.  It's important to bear in mind though that those builders are abstracting the process away from pure WordPress Templates.  If we're going to create a theme that will work within WordPress then we are going to have to ensure that we use the correct Templates amd most importantly we name them correctly.

There are two articles in the WordPress Developer Documentation that are worth consulting at this point.

1.  [Template Files](https://developer.wordpress.org/themes/basics/template-files/)
2.  [Template Hierachy](https://developer.wordpress.org/themes/basics/template-hierarchy/)

These have been precised nicely in [Pinegrow's own documentation](https://pinegrow.com/docs/wordpress/a-guide-to-wordpress-templates-for-posts-pages-and-custom-post-types/).

### Practicality

If you've glanced at the documents we referred to above then you'll realise that there are a number of templates that we should definitely include.

|   Template Name|   Purpose	|
|---	|---	|
|   index.php 	|  The ultimate fallback 	|
|   home.php	|  The main standard posts archive 	|
|   front-page.php|  Used to display a static front page if there is one 	|
|   page.php 	|   Used to display single posts	|
|   single.php 	|   Used to display single pages	|
|   archive.php	|   Used to display groups of related posts	|
|   404.php 	|   Used as a catch all for non existent posts or pages	|




There are also going to be templates that will be required to allow end users to create their own pages or posts. Typically you'll provide these to allow end users to create pages or posts that follow a particular pre-defined structure.


### Style / CSS

With regard to WordPress themes this is something of an esoteric subject.  Your Theme will need to be styled with Cascading Style Sheets (CSS) and this will cover all of the visual layout ( colours, fonts layout etc). You are free to use plain vanilla css or one of the many css frameworks that are available.  

For maximum flexibility then you should be using plain css as defined in the [W3Schools](https://www.w3schools.com/css/). This will allow end users using your theme to add thier own style overides with little chance of their breaking anything that you have provided.  

There are some very good well known css frameworks and there is nothing wrong with using these but you may well have to be more rigid in whaat you allow end uers to do of their own volition.