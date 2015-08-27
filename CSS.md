##More HTML and Stylesheets

###Add some elements to the page

Before we take a look at adding some style to our page, let's add a few more elements to our web page. While you can make everything in your web page with the \<h1> and \<p> tags for headers and paragraphs, it it helpful to have some other items in your page. Some of these items will be more informative about the text that is inside of the tag.

In HTML5 we have a number of elements that actually describe the content that we have on the page better. For example, instead of just having an \<h1> tag, we can add a \<header> tag to be clear that this is a header for the document or a section. Similarly, we can also set a \<footer> for the bottom of the document or section.

Let's add a header to the top of your "index.html" page. Here we added a \<header> tag around our \<h1> tag.

````
<body>
	<header>
		<h1>Visit Anytown, USA!</h1>
	</header>
````

Let's add a footer to our page as well. Many web pages will use a footer to contact information as well as a Copyright for the information on the page. Let's add one now.

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

Next, copy an image to this folder and then we can add it to part of your web page with an \<img> tag. Notice that the "src" attribute is pointing to where the image is stored. This could also be an image stored on another server.

````
<img src="images/picture1.jpg" />
````

###Adding Hyperlinks
Finally, let's learn how to add links to other locations. We will use an anchor tag for this, and we'll start with something simple like text. Here, we have an example of a hyperlink to an online shopping site. Notice, that the "href" attribute is the URL or address of the page that we are linking to and the "Click Here to Shop" is what is displayed to the user.

````
<a href="http://amazon.com">Click Here to Shop</a>
````

We can change this to a more interesting link like an image if we change the content of the anchor tag (\<a>). For example, the following is the same hyperlink, but we are using a logo for the item to click. There is no text displayed as part of this hyperlink.

````
<a href="http://amazon.com"><img src="images/amazonlogo.jpg" /></a>
````

###Now for some style
Now that you have a few more items to work with in your HTML, let's look at some ways that we can make thinks look a little more stylish than plain black and white text.

We have already seen that using different tags will make items display in different sizes, but we can also use what are called styles. There are two different ways we can do styles. The first is with inline styles where we add a description of how we want the text to appear in the middle of our HTML.

````
<p style="color=red;text-align=center">some text</p>

````

If I have a lot of paragraphs on my page and I want them to all look this way, I would have to put this style on each paragraph. The challenge with using this type of style is that if I want to change all the paragraphs that are red throughout my website...there's potentially a lot of work to do.

So we turn the a second (and preferred) method of linking a stylesheet to our page. This stylesheet tells how to render items in our web page and applies it consistently across all items. The way we determine how the styles are applied are based on "selectors" or selection criteria. Additionally, we can have multiple stylesheets loaded and they will add all of their styles collectively. This is why they are called "Cascading Style Sheets" (which is why they have an extension ".css")

In the example below, we are loading a stylesheet called "app.css" that will contain our web page specific styles.

````
<link href="app.css" rel="stylesheet" />
````

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

Save you "app.css" and refresh your browser to see how it looks.

Let's move on to the body of the web page. Let's take the two lists that we have and put an HTML tag for an \<aside> around them to show they are not a main part of the content. 

````
<aside>
	<h2>Things to Do</h2>
	<ol>
		<li>Hiking</li>
		<li>Biking</li>
		<li>Horseback</li>
		<li>Backpacking</li>
	</ol>
</aside>

...

<aside class="col-sm-2">
	<h2>How to Get Here</h2>
	<ul>
		<li>By Plane</li>
		<li>By Train</li>
		<li>By Automobile</li>
		<li>By Boat</li>
	</ul>
</aside>
````

Finally, for the rest of the body, let's define this as a \<section>. All of the content between our two \<aside> lists will be surrounded by this \<section> tag.

Now, let's set the colors and alignment for our lists.

````
aside {
	background-color: #aaa
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

Oops! We have a problem. All of the \<h2> tags were updated to be red and that is not what we wanted. We only wanted our list titles to be red.

One of the ways we can fix this is to change our selectors to be more specific. For example, the following selector would tell the style only to be applied to \<h2> tags inside of the \<aside> tag.

````
aside h2 {
	color: red;
}
````

Another way to fix this is by adding a class to the \<h2> in our lists and call it "listtitle".

````
<aside>
	<h2 class="listtitle">Things to Do</h2>
	<ol>
		<li>Hiking</li>
		<li>Biking</li>
		<li>Horseback</li>
		<li>Backpacking</li>
	</ol>
</aside>
````

Now we can tell our stylesheet to apply the red color not to the \<h2> tag, but to the "listtitle" class. Notice in the selector, we are telling it to use a class by starting the with a dot.

````
.listtitle {
	color: red;
}
````

Save and refresh to see your list titles updated.

We can mix and match selectors for tags and classes to get pretty specific about the items we are asking to style. There is an additional selector for a tag with a specific id (we use "#" instead of the "." dot). First you would add an "id" attribute to your html tag.

````
<aside>
	<h2 class="listtitle">Things to Do</h2>
	<ol id="todolist">
		<li>Hiking</li>
		<li>Biking</li>
		<li>Horseback</li>
		<li>Backpacking</li>
	</ol>
</aside>
````
Then add whatever styling elements that you needed to make it look right for your design.

````
#todolist {
	color: green;
}
````

There is WAY MORE to CSS than we have covered here. If you want to see the potential of CSS, you can take a look at http://csszengarden.com. This is a collection of pages that use the exact same HTML, but have a different stylesheet applied. As you click through the different designs, you will see the creativity and design that can come alive with styles.
