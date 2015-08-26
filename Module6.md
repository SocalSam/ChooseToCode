##Module 6 - Intro to BootStrap

###Objectives
 - refactor existing website to use Bootstrap for layout

###Adding Bootstrap to our web site

In order to begin using Bootstrap on our web page, we need to include it in our web page. There are two pieces to the Bootstrap framework: Stylesheets (CSS) and JavaScript (js). We could download these to our own working folder, but for now, we are going to use a Content Delivery Network to give us the version of Bootstrap we want.

We're going to add the two Bootstrap files to our \<head> tag in our web page like this:

````
<head>
	<title>My First Web Page</title>
	<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet" />
	<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.jss" rel="text/javascript" />
	<link href="app.css" rel="stylesheet" />
</head>

````

At this point nothing has changed on our page. Adding the Bootstrap files gave us access to the CSS classes that will define how our page gets laid out on different devices.

###Adding Containers
Bootstrap is based on having a container element to wrap all of the site contents and manage the rows that will lay out the 12 column grid system.

We are going to use the "container-fluid" class to make a full width container that will resize based on the size of the browser viewport.

Let's start by adding this class to our page \<header>.

````
<header class="container-fluid">
	<h1>Visit Anytown, USA!</h1>
</header>
````

Next, do the same around the main part of our web page including the both \<aside> and the \<section> tags that contain the bulk of the page content. Since we are working with three groups of tags, add a \<div> to wrap all of the page content not in the \<header> or \<footer>.

````
<div class="container-fluid">
	<aside>
	...
	</aside>
</div>
````

Finally, add the "container-fluid" class to the footer of your page.

````
<footer class="container-fluid">
	Copyright 2015
</footer>
````

Save and view your web page in a browser. Resize the width of your browser and see how the header and footer resize as well as the content in the page.

###Now for the Rows
Next, we want to move on the main content of our web page. Once we have our containers, we can create a row inside of that container. That row will be the basis for our twelve columns in our grid. Any time we are working with a row, we want to keep in mind that the number of columns should always add up to twelve.

In our example web page, we want to have the first list take up two columns, the main content to take the next eight columns and finally our second list to fill the final two columns.

First, change both \<aside> tags to have a class of "col-sm-2". This means on all devices small and up, create a space that is two grid columns wide.

````
<aside class="col-sm-2">
````
Next, change the 

````
<section class="col-sm-8">
````

Save and view. Resize the window to see reflow.

````
<article class="row">
	<h2>Amazing Museums</h2>
	<div class="col-sm-3">
		<img src="http://lorempixel.com/200/100/city/1" />
	</div>
	<div class="col-sm-9">
		<p>While most museums are a collection of old artifacts and stuff that no one is really interested in seeing, our musuems
			are the best of the best.</p>
		<p>You won't find anything like these any where else in the world. Our museums rival that of our closest competitors including
			the Museum of Bad Art, the Paris Sewers Musuem and the Museum of Broken Relationships.</p>
		<p>Come check them out...the fun is waiting for you.</p>
	</div>
</article>
````

- Layout
- Mobile Dev
- Responsive Design