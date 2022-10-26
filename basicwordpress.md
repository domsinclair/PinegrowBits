# Creating a basic WordPress site using Pinegrow

This tutorial is aimed at those people who generally create websites based on the WordPress CRM and especially for those who have generally used specific WordPress page builders to accomplish that task.

This tutorial is going to use the BaseTheme that we developed and then imported into Pinegrow as our staring point.  If you haven't read those yet then it will help your understanding of what is to follow if you do so now.

[How to create a basic Tailwind site](basicsite.md)

[How to setup a Pinegrow Project from the basic tailwind site](pgbasictemplate.md)

Whilst the tasks involved are actually relatively straight forward the subject matter needs to be understood.  Conventional Page Builders abstract away a lot of the mechanics about how WordPress sites actually work.  If you are going to be a proficient WordPress site creator using Pinegrow then you will need to develop a sound understanding of these principles.  Whilst this tutorial will try and address this it should not be seen as a single source of truth on the matter.

## Getting Started

### Creating a local WordPress site

Before we get started there is one task that we need to do.  We are going to need a local WordPress site on our development machine for testing purposes.

---
**NOTE**

When the new Pinegrow WordPress plugin is released this step will not be strictly necessary. If you are using the desktop version though it is.

___

For this task we're going to use [Local](https://localwp.com/).  Download and install the program.  Once you have done that open it and create a new site.  It's a relatively straight forward procedure. You can customise the site that is created choosing the version of PHP required, the server type it will be run on and the version of MySql for the database.  It makes sense to try and replicate the settings that are available obn the final hosting domain.


### Configure Pinegrow for WordPress

Open up Pinegrow and the open up the project that was created in the second tutorial.  Once open, open up the index.html file.  Clear out the content with the body section so that the actual html looks like this;

```html
<!doctype html>
<html>
    <head>
        <meta charset="UTF-8"/>
        <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
        <link href="tailwind_theme/tailwind.css" rel="stylesheet" type="text/css"/>
    </head>
   <body>
    
   </body>
</html>
```

When creating content for WordPress Pinegrow lets you build Themes or Plugins.  To begin with we are going to create a theme.  There's no need to feel daunted by this, Pinegrow is going to do almost all of the work for you.  Concentrate instead on what it's doing, and how this relates to the way that WordPress wesites need to be built.

In Pinegrow click on the WordPress icon to open the WordPress tool panel and click the Activate WordPress button.



![image Terminal Window](./images/tutorial3/img1.jpg)

You will now see the following dialog

![image Terminal Window](./images/tutorial3/img2.jpg)

There are a number of options in this dialog but for the time being we really only need to fill in the three required fields as we will keep the default Project Type of Theme as is;

![image Terminal Window](./images/tutorial3/img5.jpg)

The theme folder is the folder that contains the WordPress themes in the new local site we created earlier.

![image Terminal Window](./images/tutorial3/img4.jpg)

---
**NOTE**

You will need to create a specific folder to hold your newly created theme files.
___

Save the settings, then from the WordPress menu Export the theme.

Navigate to your newly created theme folder and look at what Pinegrow has just created for you.

![image Terminal Window](./images/tutorial3/img6.jpg)



### Adding the basics to our theme


There is a wealth of documentation on WordPress themes in the official [WordPress Developer Documentation](https://developer.wordpress.org/themes/).  This can seem a daunting read, especially to anyone not familiar with the intricacies of writing code and especially to those WordPress developers who have only ever used Page Builders.  However the fundamentals are not that complicated to understand and we'll see that Pinegrow has already got us off to a good start.

Typically one of the first things that you'd do would be to create templates which would be used to render content.  On first glance there is no obvious way to do this in Pinegrow, however Pinegrow works with WordPress as defined by its documentation.

Before we continue consider this image from the WordPress documentation.

![image Terminal Window](./images/tutorial3/img3.jpg)

What is being depicted here is a visual representation of the WordPress template hierarchy. Working from left to right we see the basic page types that we find on a typical WordPress site.  The diagram demonstrates how these page types are rendered by a series of secondary, variable and finally primary templates. On the far right, acting as a catch all for everything is the index.php template. In essence the index.php template is what a tradition page builder might describe as a Main or Master template.

---
**NOTE**

WordPress templates are php files.
___

Look back at the WordPress settings images above and notice that the Master Page by default had been set to the index.html file and if you then look at the files that were added to our new theme directory in the local site you'll see that we already have an index.php file created for us by Pinegrow. 


## The Main Catch All Template (index.php)

We'll now set about adding some content to our index.html page and in the process create what will become the master template for our new wordpress theme.  Before we get started on that we need to take some time to give newcomers to Pinegrow some basic information on how to get things done.

### Using Pinegrow

This is not going to be an exhaustive dissertation on how to use Pinegrow, for that [see the documentation](https://pinegrow.com/docs/getting-started/), rather this will act as a brief introduction to those bits that you need to familiarise yourself with.  

![image Terminal Window](./images/tutorial3/img7.jpg)

On the left hand side of the main screen click on the Library icon to open the Library panel, do the same on the right hand side with the structure panel.

Pinegrow is essentially an html editor so the first thing that you'll see in the library is a comprehensive list of all the possible html tags that you can place on your pages.  If you're familiar with html this may be all that you need to get started.  Html tags can be dragged from the library onto the main surface of your page and those will inturn appear in the newly opened structure panel on the right.

For many users of page builders this may seem a little too basic as they have been used to dragging ready made components onto pages / templates that they are creating. Pinegrow can help you there as it has a series of ready made blocks to get you started. In the library panel click on the Blocks tab.


![image Terminal Window](./images/tutorial3/img8.jpg)

Take some time to scroll through some of the ready made items that Pinegrow have provided to use with Tailwind CSS.


---
**NOTE**

There are a number of pre-built components for Tailwind that can be found all over the internet. Below are just a couple of good examples.

TailwindCSS themselves make a comprehensive set [TailwindUI](https://tailwindui.com/components). These are paid for components. <br>
[Flowbite](https://flowbite.com/) Both free and paid for components.
___


### Creating the index.html page

To keep things simple for the moment we'll use the pre-designed blocks that Pinegrow have provided.

From the blocks tab in the library select the Headers section and find the Fullwidth menu,  It's not the most spectacular header design wise but it will do for what we require.  Drag it to your page and you'll have a header section at the top.

Next up we are going to need a footer section.  From the blocks find the footers and drag Footer Block 2 onto the page.

The page should now look like this

![image Terminal Window](./images/tutorial3/img10.jpg)

We have a header at the top and a footer at the bottom.  Now all we need is something in the middle to act as a container for the rest of the templates we will create.


Return to the list section of the Library. Find the sections section and from there drag a section tag into the structure tree to sit between the header and footer. With the section still selected open the WordPress panel and scroll down through the WordPress actions until you find Site Content.  Select that.  

In the structure tree locate the div in the header section that contains the menu items.  Add a WordPress Menu action to it.

Now save the page and Export the theme.


### Creating the page.html page

If you refer back to the visual diagram of the WordPress template layout from earlier you'll see that single blog posts and pages get displayed via the page.php template.

In the project panel click on the little drop down arrow next to the project name and from the drop down menu select Create a new File.  In the dialog that opens name this page.html and click OK.

