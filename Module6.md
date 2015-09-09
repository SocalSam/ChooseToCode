##Module 6 - Intro to BootStrap

###Objectives
 - refactor existing website to use Bootstrap for layout

###Adding Bootstrap to our web site

In order to begin using Bootstrap on our web page, we need to include it in our web page. There are two pieces to the Bootstrap framework: Stylesheets (CSS) and JavaScript (js). We could download these to our own working folder, but for now, we are going to use a Content Delivery Network to give us the version of Bootstrap we want.

In the index.html page, we're going to add the two Bootstrap files to our \<head> tag like this:


```HTML
<head>
	<title>My First Web Page</title>
	<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet" />
	<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js" rel="text/javascript" />
	<link href="app.css" rel="stylesheet" />
</head>

```
We could have downloaded these to our machine, but we are going to take advantage of the content delivery network for the bootstrap files. This takes the load off of our web server and potentially serves the file to the user faster.

At this point nothing has changed on our page. Adding the Bootstrap files gave us access to the CSS classes that will define how our page gets laid out on different devices.

###Adding Containers
Bootstrap is based on having container elements that wrap all of the site contents. These containers then are subdivided into rows that each have 12 columns. We will then use classes to mark our code up for how many columns each set of content will take.

Let's start with containers. We are going to use the "container-fluid" class to make a full width container that will resize based on the size of the browser viewport.

Let's start by adding this class to our page \<header> in the "index.html" file.

```HTML
<header class="container-fluid">
	<h1>Visit Anytown, USA!</h1>
</header>
```

Next, add another \<div> that will surround the main part of our web page including the both \<aside> and the \<section> tags that contain the bulk of the page content. Be sure to include all of the content except the \<header> or \<footer>.

```HTML
<div class="container-fluid">
	<aside>...</aside>
	<section>...</section>
	<aside>...</aside>
</div>
```

Finally, add the "container-fluid" class to the footer of your page.

```HTML
<footer class="container-fluid">
	Copyright 2015
</footer>
```

Save and view your web page in a browser. Resize the width of your browser and see how the header and footer resize as well as the content in the page.

###Let's Add Some Navigation
Just under our header, we are going to use bootstrap to add a navigation menu to our page. We'll keep it simple, but Bootstrap will take care of everthing for us including the highlights and layout.

```HTML
<header class="container-fluid">
	<h1>Visit Anytown, USA!</h1>
</header>
<nav class="container-fluid">
	<ul class="nav navbar-inverse navbar-nav">
		<li class="active"><a href="#">Home</a></li>
		<li><a href="http://www.bing.com/search?q=amazing%20places">Amazing Places</a></li>
		<li><a href="#contact">Contact</a></li>
	</ul>
</nav>
```

Before we take a look at the navigation we just added, let's add just a little styling to it so it will look nice. In the "app.css" file, let's add the following styles

```CSS
nav {
	background-color: #222;
}

section, article {
	padding: 10px;
	background-color: #eee;
}

img {
	height: 100%;
	width: 100%;
}
```
Save and load the "index.html" file in your browser and notice the new navigation menu. As you resize your browser to a narrow window, you will see that the menu items go from being on the same line to being on their own lines. Thanks to Bootstrap, we don't have to spend a lot of time building this custom menu functionality.

We will add the content for the "Contact" link a little later in this module. Let's get back to Bootstrap layouts.

###Now for the Rows
Next, we want to move on the main content of our web page. Once we have our containers, we can create a row inside of that container. That row will be the basis for our twelve columns in our grid. Any time we are working with a row, we want to keep in mind that the number of columns should always add up to twelve.

In our example web page, we want to have the first list take up three columns, the main content to take the next six columns and finally our second list to fill the final three columns.


In the "index.html file, just after the \<div> surrounding our main content, add another \<div> and give it a class of "row".

```html
<div class="container-fluid">
	<div class="row">
		<section>
```

We are now ready to subdivide the row with our content into the columns. Change both of the \<aside> tags to have a class of "col-sm-3". This means on all devices small and up, create a space that is three grid columns wide.

```HTML
<aside class="col-sm-3">
```
That will account for six of the columns in our grid, so now we want to change the main section of our content to have a class of "col-sm-6" to account for the other six columns.

```HTML
<section class="col-sm-6">
```

Save and view "index.html" in a browser. Notice that the two lists we created now float to the right and left of our main content. What happens when you resize the window to a narrow screen similar to a phone? The our content automatically reflows as necessary.

###More rows
Now that the content flows a little better when we resize the browser, let's take a closer look at our main content.
We're going to make the content of the articles flow a little nicer with devices as well.

In the "index.html" file, lets add a \<div> with a class of "row" to the main section.

```HTML
<section class="col-sm-6">
	<div class="row">
		<h2>Amazing Museums</h2>

	...

	</div>
</section>
```

This will give us another row with a 12 column grid that we can begin to lay each article out. Let's make the image take up three columns and the paragraphs fit in the other nine columns. Repeat this for each of the articles on the page.

```HTML
<article>
	<h2>Amazing Museums</h2>
	<div class="col-sm-3">
		<img src="http://lorempixel.com/175/100/city/1" />
	</div>
	<div class="col-sm-9">
		<p>While most museums are a collection of old artifacts and stuff that no one is really interested in seeing, our musuems are the best of the best.</p>
		<p>You won't find anything like these any where else in the world. Our museums rival that of our closest competitors	including the Museum of Bad Art, the Paris Sewers Musuem and the Museum of Broken Relationships.</p>
		<p>Come check them out...the fun is waiting for you.</p>
	</div>
</article>

```
Save your work and load the "index.html" file in a browser. Try resizing the browser, and notice how the articles now flow nicely even on very narrow screens.


###A Little Bit of Tug-o-war
When the content reflows, things tend to jump around. The question you have to ask, is "What is the most important content to be showing?" Currently, in a wide layout, our content is showing the main content between our two lists. When we resize the browser window to a narrow view, the main content is still between our two lists. What if we wanted to show our main content first? We need to reorder our content to help us out here. Let's do that now.

Move the \<section> tag and all of it's content above the first \<aside> content.

```HTML
<section class="col-sm-6">...<\section>
<aside class="col-sm-3">...</aside>
<aside class="col-sm-3">...</aside>
```

Save and reload the page in the narrow format. We got the look that we wanted. What about when we go back to the wide view? Things don't look the way we really want them now. The lists are both on the right side of the web page and it isn't what we wanted. Do we have to create two views of the data for this?

###Bootstrap Push and Pull

Thankfully, Bootstrap has a few extra classes that allow us to flow the content to where it needs to go. We put the content in the order that we want it to flow, then we use the Bootstrap classes to tweak the details for the layout. Let's look at the Bootstrap "push" and "pull" classes.

First, let's modify the page so that the main content within the <section> tag is first, followed by our two aside tags. To do this, I simple cut the first <aside> section and move it under the </section> tag

```HTML
            <section>
            ...
            </section>
            
            <aside class="col-sm-3">
                <h2 class="title">Things to Do</h2> 
                <ul>
                    <li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
                    <li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
                    <li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
                    <li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
                </ul>
            </aside> 
```

We will modify the main \<section> class by telling it to push three columns to the right.

```HTML
<section class="col-sm-6 col-sm-push-3">...</section>
```

Next, modify the first \<aside> class by telling it to "pull" six columns to the left.

```HTML
<aside class="col-sm-3 col-sm-pull-6">...</aside>
```

Save and reload the page and look at the difference between the narrow width and the wide width browsers. Notice now the most important content is where it needs to be for each type of display.

###About that Contact Info
Now that you have seen how to do column push and pull, let's add the content for our Contact information.

Because we added a link to our contact information, we will want to put in some HTML for that at the bottom of our page. Notice that putting the "name" attribute on the \<a> tag it becomes a hyperlink that I can quickly forward a user to.

```HTML
<div class="container-fluid">
	<div class="row">
		<div class="col-sm-6 col-sm-push-3"></div>
		<div class="col-sm-6 col-sm-pull-3">
			<a name="contact">Contact Us</a>
			<p>Anytown Chamber of Commerce</p>
			<p>123 Main St.</p>
			<p>Anytown, OH 43210</p>
		</div>
	</div>
</div>
```

Save your work and reload the page. Then use the "Contact" link in the navigation menu to scroll to the Contact information on the page. Be sure to check the behavior in both the full screen experience as well as a narrow small screen experience.

###Push the changes to Azure
To close out this module, let's check in our changes and push them to Azure. You should already be set up for this from the previous modules, so if you haven't done the push to Azure before, you will need to back up and do that module first.
From a "Git Shell" prompt, we will do the following steps:

 1. Add all of the changed files to a checkin
	
	````
	git add .
	````
 2. Commit all of the changed files to your local repository

	````
	git commit -m "Added bootstrap styling"
	````
 3. Push all of the code changes to your Azure repository

	````
	git push azure master
	````

Now, navigate to your website at http://yourwebsite.azurewebsites.net and confirm that your code has been deployed.
