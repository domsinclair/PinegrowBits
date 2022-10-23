# How to create a basic Tailwind site

This tutorial will walk you through the basics of creating a simple website with a single page that utilises Tailwind CSS. The code that makes up this tutorial is available as a separate download and it can form the base for a Pinegrow project.

I would like to take the opportunity of thanking Adam Lowe of [Peak Performance Digital](https://peakperformancedigital.com/) for his time in proof reading the original of this and making some very pertinent suggestions as to how to do all this properly.

We'll be using Visual Studio Code to create our base project.  If you don't have a copy of it you can [download it from here](https://code.visualstudio.com/download).

Once you have Visual Studio Code installed(herein and after referred to as VSCode)  you're also going to need to install Node JS which you can [get from here](https://nodejs.org/en/download/). Select the version that best suits your operating system and it probably makes more sense to opt for the LTS version rather than the latest version.

At a location of your choice on your computer create a new folder called BaseTheme.

---
**NOTE**

Do Not have any spaces in your folder name as this can cause issues later on when importing this into Pinegrow.

___

Open VSCode and then within that open your newly created folder.  Once open go to the Terminal menu in VSCode and then click New Terminal. A terminal (command) window will open up at the bottom of the editing window.

![image Terminal Window](./images/tutorial1/img1.jpg)

The first task is to creat a Package .Json file.  At the command prompt type in the following command.

`npm init -y`

![image Terminal Window](./images/tutorial1/img2.jpg)