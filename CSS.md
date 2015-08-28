﻿##More HTML and Stylesheets
^**Note:** *************BEGIN***************
^**Note:** 
^**Note:** 
^**Note:** 
^**Note:** ************* END ***************

###Add some elements to the page

Before we take a look at adding some style to our page, let's add a few more elements to our web page. While you can make everything in your web page with the \<h1> and \<p> tags for headers and paragraphs, it it helpful to have some other items in your page. Some of these items will be more informative about the text that is inside of the tag.

^**Note:** *************BEGIN***************
^**Note:** Is is correct to assume that the previous md file was read?
^**Note:** ************* END ***************

In HTML5 we have a number of elements that actually describe the content that we have on the page better. For example, instead of just having an \<h1> tag, we can add a \<header> tag to be clear that this is a header for the document or a section. Similarly, we can also set a \<footer> for the bottom of the document or section.

Let's add a header to the top of your "index.html" page. Here we added a \<header> tag around our \<h1> tag.

````
<body>
	<header>
		<h1>Visit Anytown, USA!</h1>
	</header>
````

Let's add a footer to our page as well. Many web pages will use a footer to contact information as well as a Copyright for the information on the page. Let's add one now.

^**Note:** *************BEGIN***************
^**Note:** Footer seems like it should be seen at the bottom of the page
^**Note:** Which it is, might want to point out that the <footer></footer> should be just above the </body>
^**Note:** It is clear in the image, but it could be missed (I did).
^**Note:** ************* END ***************
````
	<footer>
		Copyright 2015
	</footer>
</body>

</html>
````

###Adding Images
Now, for a little visual appeal, we want to add some images to our text. Usually, these images will be in a folder on your website, but they could really come from anywhere as long as you know the URL.

Let's create a folder for images and then link an image to your web page.

![images folder](images/images-folder.png?raw=true)
^**Note:** *************BEGIN***************
^**Note:** Image shows the file app.css, how did that happen?
^**Note:** Either add App.css addition to Code or change image (sorry)
^**Note:** ************* END ***************

Next, copy an image to this folder and then we can add it to part of your web page with an \<img> tag. Notice that the "src" attribute is pointing to where the image is stored. This could also be an image stored on another server.

^**Note:** *************BEGIN***************
^**Note:** Might note that the image name will be different.
^**Note:** Not sure if this would cause confusion, but if I drag an image in, the name will be different
^**Note:** But attempt at clarification might lead to more and inefficient words.  The other server comment could be deleted.
^**Note:** ************* END ***************

````
<img src="images/picture1.jpg" />
````

###Adding Hyperlinks
Finally, let's learn how to add links to other locations. We will use an anchor tag for this, and we'll start with something simple like text. Let's take our list of things to do and make hyperlinks to a search engine.

````
<h2>Things to Do</h2>
<ol>
	<li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
	<li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
	<li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
	<li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
</ol>

````

We can change hyperlinks to a more interesting link like an image if we change the content of the anchor tag (\<a>). For example, in the following hyperlink, we are using an image for the item to click. There is no text displayed as part of this hyperlink.
^**Note:** *************BEGIN***************
^**Note:** Where did I get this image?  Well of course this ties back to you mention of using other servers.
^**Note:** But HS Students sometimes have short attention spans, mostly the ones who will become managers (haha)
^**Note:** Difficult to easily implement.  Where did I get the image?  Does it have to be a jpg?
^**Note:** ************* END ***************

````
<a href="http://microsoft.com"><img src="images/microsoftlogo.jpg" /></a>
````
So now we have a link to the Microsoft web site and the logo will be what the user sees to click on.

###Now for some style
Now that you have a few more items to work with in your HTML, let's look at some ways that we can make things look a little more stylish than plain black and white text.

We have already seen that using different tags will make items display in different sizes, but we can also use what are called styles. There are two different ways we can do styles. The first is with inline styles where we add a description of how we want the text to appear in the middle of our HTML.

````
<p style="color:red;text-align:center">some text</p>

````

If I have a lot of paragraphs on my page and I want them to all look this way, I would have to put this style on each paragraph. The challenge with using this type of style is that if I want to change all the paragraphs that are red throughout my website...there's potentially a lot of work to do.

So we turn the a second (and preferred) method of linking a stylesheet to our page. This stylesheet tells how to render items in our web page and applies it consistently across all items. The way we determine how the styles are applied are based on "selectors" or selection criteria. Additionally, we can have multiple stylesheets loaded and they will add all of their styles collectively. This is why they are called "Cascading Style Sheets" (which is why they have an extension ".css")

In the example below, we are loading a stylesheet called "app.css" that will contain our web page specific styles.

````
<link href="app.css" rel="stylesheet" />
````
^**Note:** *************BEGIN***************
^**Note:** For some reason this seems confusing, of course that could just be me
^**Note:** Not a show stopper, but take a look at clarification or emphasis of the addition of file.
^**Note:** ALSO and important, where do I put the <link...> line?  Where to put stuff is confusing to students new to HTML
^**Note:** ************* END ***************
Let's do that now with your existing "index.html" page we have already created. First create a new file called "app.css" in the same folder as your index.html file and add the above \<link> to the stylesheet.

![Add app css](images/add-app-css.png?raw=true)

Now it's time to add some flair to your web page. First, let's change the look of our header and footers that we created. For this, we are going to use the tag selectors for \<header> and \<footer>. Notice that we just use the tag name and then we have a list of style attributes we want to set. We are going to use the "background-color" attribute. In order to set the color, we can use a color name like "red" or we can use a color value. To use a color value, you start with a hash symbol and then specify three values for red, green and blue. These values go from 00 through FF. We call these a hex value short for hexadecimal...or a number system with 16 values (0-F). So "#000000" will be 0 for Red, 0 for Green and 0 for Blue...or the color black. Sometimes you might see this short cut to just three numbers like "#ddd" which is the same as "#dddddd".

Let's make the header and footer a dark grey. At the same time, let's use the "color" attribute to make the text color a lighter grey.

````
header, footer {
	background-color: #4a4a4a;
	color: #ddd;
}
````
^**Note:** *************BEGIN***************
^**Note:** Following the instructions made the whole page background dark
^**Note:** 
^**Note:** 
^**Note:** ************* END ***************

Save your "index.html" and "app.css" files and reload the index.html in your browser. Your header and foother should now be light grey on a dark grey.


Now let's add some visual space around our text with some "padding". It might also look nice to center our text so let's go ahead and add that too.

````
header, footer {
	background-color: #4a4a4a;
	color: #ddd;
	padding: 20px;
	text-align: center;
}
````
^**Note:** *************BEGIN***************
^**Note:**  ...you...
^**Note:** ...your...
^**Note:** 
^**Note:** ************* END ***************
Save you "app.css" and refresh your browser to see how it looks.

Let's move on to the body of the web page. Let's take the first list that we have and put the HTML tag \<nav> around it to show they are not a main part of the content. Typically, we would use this tag to identify a navigation menu.

````
^**Note:** *************BEGIN***************
^**Note:** Why did I add the <nav> tag?  When I refresh my browser there is no obvious changes.
^**Note:** Nav, aside css code works,
^**Note:** 
^**Note:** ************* END ***************
<nav>
	<h2>Things to Do</h2>
	<ol>
		<li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
		<li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
		<li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
		<li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
	</ol>
</nav>
````

Next, lets put a tag around the second list to call it out as not being part of the main content. In this case, we will use the \<aside> tag.

````
<aside>
	<h2>How to Get Here</h2>
	<ul>
		<li>By Plane</li>
		<li>By Train</li>
		<li>By Automobile</li>
		<li>By Boat</li>
	</ul>
</aside>
````
^**Note:** *************BEGIN***************
^**Note:** Following the practice of showing the students where to put tags, show where the <section> tags goes
^**Note:** 
^**Note:** 
^**Note:** ************* END ***************
Finally, for the rest of the body, let's define this as a \<section>. All of the content between our \<nav> and \<aside> lists will be surrounded by this \<section> tag.

Now, let's set the colors and alignment for our lists.

````
nav, aside {
	background-color: #0aa
	text-align: center;
	padding-top: 40px;
}
````

One more little change here, let's change the text in the  \<h2> tag to the color red.

````
h2 {
	color: red;
}
````
Now, save and refresh your browser to see the formatting updates that we have made.

Oops! We have a problem. All of the \<h2> tags were updated to be the red and that is not what we wanted. We only wanted our list titles to be red.

One of the ways we can fix this is to change our selectors to be more specific. For example, the following selector would tell the style only to be applied to \<h2> tags inside of the \<aside> tag.

````
aside h2 {
	color: red;
}
````

Another way to fix this is by adding a class to the \<h2> in our lists and call it "listtitle".

````
<nav>
	<h2 class="listtitle">Things to Do</h2>
	<ol>
		<li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
		<li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
		<li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
		<li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
	</ol>

</nav>
````

Now we can tell our stylesheet to apply the red color not to the \<h2> tag, but to the "listtitle" class. Notice in the selector, we are telling it to use a class by starting the with a dot.

````
.listtitle {
	color: moccasin;
}
````

Save and refresh to see your list titles updated.

We can mix and match selectors for tags and classes to get pretty specific about the items we are asking to style. There is an additional selector for a tag with a specific id (we use "#" instead of the "." dot). First you would add an "id" attribute to your html tag.

````
^**Note:** *************BEGIN***************
^**Note:** Could the todolist be confusing?  What about activitieslist or sportslist
^**Note:** 
^**Note:** 
^**Note:** ************* END ***************
<nav>
	<h2 class="listtitle">Things to Do</h2>
	<ol id="todolist">
		<li><a href="http://www.bing.com/search?q=hiking">Hiking</a></li>
		<li><a href="http://www.bing.com/search?q=biking">Biking</a></li>
		<li><a href="http://www.bing.com/search?q=horseback">Horseback</a></li>
		<li><a href="http://www.bing.com/search?q=backpacking">Backpacking</a></li>
	</ol>
</nav>
````
Then add whatever styling elements that you needed to make it look right for your design.

````
#todolist {
	color: green;
}
````

There is WAY MORE to CSS than we have covered here. If you want to see the potential of CSS, you can take a look at http://csszengarden.com. This is a collection of pages that use the exact same HTML, but have a different stylesheet applied. As you click through the different designs, you will see the creativity and design that can come alive with styles.
