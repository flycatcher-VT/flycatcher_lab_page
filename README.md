# Matute Lab Website

This is the website of our academic research group at UNC chapel Hill.

We would like to thank the Allan lab (https://www.allanlab.org/) for letting us copy their website template /repo.
If you would like to learn more, please visit their lab page.

To the next Technical Support Person in the Matute Lab: This README.md is for you. I will try to give a short description
of how to set up the environment to edit the lab page, and how to make changes to the lab page after the environment is set up.
In general, I do not expect that there will be massive changes to the HTML structure of the page by the time the responsibility 
of management comes to you. However, I do expect that 


The Lab website utilizes Github Pages, a free alternative for hosting HTML pages through a personal GitHub repository. 
If you are asking "Whats a Github Repository?" I suggest going to this link and setting up an account: 
    
    https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github

Then, read this page to understand what a repository is (repo) and how to utilize them. 

    https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories

In short, Github is a means of version control for your code; it allows you to document changes in programs or scripts,
and allows your code to be shared and collaborated on remotely.

!!! Before you start editing the lab page, I highly suggest you familiarize yourself with the github workflow (push, pull, etc) !!!

Now that you understand what github is, you will need a way to interact with your repository locally. There are many ways to do this,
but for our purposes I would recommend using Visual Studio Code (VScode) or the online github editing feature. If you are comfortable with 
coding tools, or are not afraid to learn some standard computer science tools, follow the next steps to access the lab page through VScode.
If you arent comfortable in coding experience, then skip to the #WEB BROWSER# section below.

VScode is an Integrated Development Environment, which in short means a program that lets you write and test code in one location. Generally,
IDEs are pretty complex and take years to completely learn, and VScode is no exception. however, It is fairly intuitive and hopefully once you are 
done reading you will be able to navigate it well enough to edit the lab page! 

First, install VScode here: https://code.visualstudio.com/download

and read this user guide : https://code.visualstudio.com/docs/getstarted/getting-started

And now we can start! once you have set up your workspace, you will need to go to my github repo here: https://github.com/Okompath/Matutelab

There should be a button to "fork" the repo in the top right corner of the page. "Forking" a repo allows you to make a personal copy of my repo 
and the code inside of it to your own github account, and any changes made to your personal copy will not affect my version of the repo. 
First, go to your repo page and click settings > pages. you should see options to make the webpage live under a URL like "https://Your_username.github.io/Matutelab".
Make it live, and follow that link to check and see if the page is running. Now that you have a copy of the lab page repo and confirmed its existence on the web, 
follow these steps to integrate github:  

    https://code.visualstudio.com/docs/sourcecontrol/github

one thing to note: you will need to use terminal input to configure some github settings to your machine. to do this, click view > terminal and configure these settings by
filling in with the same info as your github account:

git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

Now you should have a means of editing your forked repo locally. in the File explorer tab in VScode (looks like two pieces of paper) you should 
see all the contents of the github repo, with dropdown menus like _data, _layouts, _pages etc. if you dont see this, i would recommend reviewing 
how to open up a github repository in VScode. Without getting into the details, the way this repository works is by using a combination of Jekyll, 
CSS, Bootstrap, and HTML to display, animate, and host our webpage. I will give a short description of each of the folders so that you may have an 
easier time of navigating and editing the page. 

While you are making edits, be sure to save and commit after every few sets of changes, then check the website periodically while you are making your 
edits to make sure they look correct. 

## _data ##
this is where the majority of repeatable data is stored, such as team members, publications, or lab updates/ news. The setup of this repo allows for 
certain pages to be dynamic, so that each page can be updated easily and without having all info hard written into each page. Each of these .yml files 
contains what essentially is a template for whatever data you want to be stored. for example, in the team_members.yml file, an entry looks like this:

- name: Daniel Matute
  photo: Daniel.png
  info: Professor
  email: dmatute@email.unc.edu
  bio : "short bio describing education, research interests, and other relevant information about the member and their role in the lab."

You can either edit an existing entry by changing each field to your intended text, or copy and paste an entry and edit it to make an additional entry. 
Make sure that there is no white space leading before the hyphen for each entry; if the indentations for an entry arent correct then they will not be 
displayed properly or at all. 


## _includes and _layouts ##

This folder is where the HTML architecture of each tab and elements in the webpage are stored. This page integrates Jekyll to convert markdown files into html, 
which then displays online. dont ask me how this works. If you ever need to change a fundamental aspect of the webpage, like color, size of an element, or something 
of the sort, i would consult the internet on the HTML coding language. I have left comments in important files that may need to be changed in the future, but if it isnt 
commented, there likely is no need for that file to be changed.

## _pages ##

This folder holds the markdown files that describe the formatting for each page. These files integrate some HTML syntax and markdown syntax, and they will be
the pages to edit if you need to change the text for a page. Anything written in blank space on the markdown file will be displayed on the webpage. 
Certain characters cause text to display differently. **Two asterisks** denote bolded text, and *single asterisks* are for italics. ## two hashtags ## create a header.
If you look closely, you can see where the data from _data is being accessed and filled in some of the pages.[text](link.com) is used to hyperlink a link to a string of text.
finally, similar to the _includes and _layouts folders, any important HTML syntax will be commented by me (text inside this <1-- text -->) to mark any important things that could 
need editing in the future.

## images ##

this folder is where all the images are stored for the lab page. teampic is for the headshots of team members and alumni, newspic is for adding images to the news.yml, and slider is for 
the slider images on the front page. to change these pictures, drag and drop them from your local machine file explorer to the vscode folder, and match the name of the image to the correct
entry in the relevant .yml file in _data.

## _sass, _plugins, css, fonts, js, downloads ##

I wouldnt mess with these, these are basic rules for the webpage.





