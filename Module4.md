#Module 4: HTML5 and the Semantic Web

###Objectives:
- Learn about HTML
- Publish a simple web page
- Plan your website
- Create your first website
- Publish your website
- Continuous Deployment

###Introduction:
So far, we have just been getting set up with the tools you need for web development. In this module we want to begin creating your first website. We will start by creating a Web App on Azure to host your website for all the world to see. Then we'll create a simple page to learn how we publish. Finally, we'll give a quick introduction to the pieces of code that are in almost every web page.
	
###Create an Azure Web App
First, let's get started with creating a place to put your new website. At this point, you need to have an active Azure subscription and a machine set up with Visual Studio Code and Git.

We are going to start at the Azure portal. With your browser, navigate to http://portal.azure.com and sign in if you need to. Go ahead and do that now and you should arrive at the portal home page.

In the upper left corner, click the plus sign or "New" button (1) to create a new Azure resource.

![Azure Portal Home](images/azure-portal-home.png?raw=true)

In the Create blade that comes up, click the "Web + Mobile" (1) option and then select "Web App" (2) to begin creating a Web App resource for your website.

![Azure Create Resource](images/azure-create-resource.png?raw=true)

Next, in the "Web App" blade that comes up, we will enter a little bit of information about your website. First, you need a name for your website. The name will be created at ".azurewebsites.net". The name will need to be unique and you should get a green checkmark (1) when you have a valid web app name. Next, you will choose the subscription to be used for your Azure web app (2). The "App Service Plan" allows you to change what region your application is hosted in and the pricing tier for your website. You can change this if you want, but you can also change this later. For now, we will skip that. Finally, leave the checkbox "Pin to Startboard" checked and click "Create" (3) at the bottom of the blade to begin creating your new Azure Web App.

![New Web App](images/new-web-app.png?raw=true)

You will be taken back to the portal home page and a new tile will show that the web app creation is in process. Once your website is up and running, you can navigate to your Web App management blade by clicking on the tile on the home page. Once you are on the Web App management blade, you can click on the link to go to your website or you can just navigate to the name of your website. For example http://ChooseToCodeTutorial.azurewebsites.net.

Since you haven't created any content yet, you should see a page that shows your web app was successfully created.

![Web App Success](images/web-app-success.png?raw=true)

There are a number of tools you can use to start publishing content to your new web application, but we are going to use a modern tool that includes version control as well.

###Publish your first web page

Now that you have a web app created for your content, we need to set you up with a way to publish your code. To do this, we are going to take advantage of a version control system built into Azure called "git".

It is important to keep track of the changes that you are making as you work on your projects. Version Control Systems keep track of those changes and allow you to experiment with your code without losing track of past work. You can always "undo" your work if you need to. This course won't cover version control, but we will use it in order to move your code into your Azure Web App.

Let's go back to the Azure Portal and take a look at the Web App blade for your website. Remember you can get to the management blade by clicking on the tile on the Portal home page. Additionally, you can also click on "Browse All" in the left navigation bar.

![Browse All](images/browse-all.png?raw=true)	

From here, you can scroll down to Web Apps and then select your website in the blade that comes up.

Once you have the Web App management blade up, scroll down to "Deployment". Click the "Set up continuous deployment" to begin setting up your source control.

![Set Up Deployment](images/set-up-deployment.png?raw=true)

In the blade that comes up for "Continuous Deployment", select "Choose Source" (1) and then "Local Git Repository" (2).

![Continuous Deploy](images/continuous-deploy.png?raw=true)

 When the "Choose Source" closes, you will see a new option for "Setup Connection" (1). Click this option to set up basic authentication for deploying your code. You will need to choose a username (2) and a password.

NOTE: The full deployment username will be the name of your website and the username you entered joined with a "\". For example: "choosetocode\username".

![Set Up Authentication](images/set-up-authentication.png?raw=true)

So now that you have your source control in place, it's time to sync up your work.

###Plan your website
Header

Footer

Body

Navigation

Images