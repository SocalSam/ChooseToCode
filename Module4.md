#Module 4: HTML5 and the Semantic Web

###Objectives:
- Learn about HTML
- Publish a simple web page
- Plan your website
- Create your first website
- Publish your website
- Continuous Deployment

###Introduction:
In this module we want to begin creating your first website. We will create a Web App on Azure to host your website for all the world to see and give a quick introduction the pieces of code that are almost every web page.
	
###HTML and your Website
First, a little about this stuff we call HTML. This stands for Hypertext Markup Langauge and is basically a fancy way of saying how do we markup a text file to make it pretty on the web. It will seems like there is a lot to learn here, but think of it as learning how to use a word processor to make fancy documents.

###Create Simple Page
Now, let's get started with creating a place to put your new website. If you have completed the first three modules of this tutorial, you should have a machine set up with Visual Studio Code, Git and an account on Azure.

We are going to start at the Azure portal. With your browser, navigate to http://portal.azure.com. If you need to sign in, go ahead and do that now and you should arrive at the portal home page.

Now, in the upper left corner, click the plus sign or "New" button (1) to create a new Azure resource.


![Azure Portal Home](images/azure-portal-home.png?raw=true)

In the Create blade that comes up, click the "Web + Mobile" (1) option and then select "Web App" (2) to begin creating a Web App resource for your website.

![Azure Create Resource](images/azure-create-resource.png?raw=true)

Next, in the "Web App" blade that comes up, we will enter a little bit of information about your website. First, you need a name for your website. The name will be created at ".azurewebsites.net". The name will need to be unique and you should get a green checkmark (1) when you have a usable web app name. Next, you will choose the subscription to be used for your Azure web app (2). Finally, click "Create" (3) at the bottom of the blade to begin creating your new Azure Web App.

![New Web App](images/new-web-app.png?raw=true)

Once your website is up and running, you can navigate to your website by clicking on the link in the Web App blade or you can just navigate to the name of your website. For example http://ChooseToCodeTutorial.azurewebsites.net.

Since you haven't created any content yet, you should see a page that shows your web app was successfully created.

![Web App Success](images/web-app-success.png?raw=true)

There are a number of tools you can use to start publishing content to your new web application, but we are going to use a modern tool that includes version control as well.

###Publish your first web page

Now that you have a web app created for your content, we need to set you up with a way to publish your code. To do this, we are going to take advantage of a version control system built into Azure called "git".

It is important to keep track of the changes that you are making as you work on your projects. Version Control Systems keep track of those changes and allow you to experiment with your code without losing track of what works. You can always "undo" your work if you need to. This course won't cover version control, but we will use it in order to move your code into your Azure Web App.

Let's go back to the Azure Portal and take a look at the Web App blade for you website. If you are not already there, you can click on the "Browse" button of the navigation bar in the Azure portal.

![Browse All](images/browse-all.png?raw=true)	

From here, you can scroll down to Web Apps and then select your website in the blade that comes up. Once you have the Web App management blade up, scroll down to "Deployment"

![Set Up Deployment](images/set-up-deployment.png?raw=true)

In the blade that comes up for "Continuous Deployment", select "Choose Source" (1) and then "Local Git Repository" (2).

![Continuous Deploy](images/continuous-deploy.png?raw=true)

 When the "Choose Source" closes, you will see a new option for "Setup Connection" (1). Click this option to set up basic authentication for deploying your code. You will need to choose a username (2) and a password.

NOTE: The full deployment username will be the name of your website and the username you entered joined with a "\". For example: "choosetocode\username".

![Set Up Authentication](images/set-up-authentication.png?raw=true)


###Plan your website
Header

Footer

Body

Navigation

Images