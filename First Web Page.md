##Your First Web Page

###Let's just start with plain text
For now, we'll start with just a text file that will tell people a little about you, a school club or a hobby you like. We'll put this in our code editor even though we are just doing text.

Let's get going by starting up Visual Studio Code. Once the editor is open, we will want to start a new folder for all of our work. Start by click "File" (1) and the "Open folder..." (2)

![VSCode File Open Folder](images/vscode-file-open-folder.png?raw=true)

In the dialog window that comes up, navigate to a good location to store your new project. Often the best place will be your "Documents" folder, but choose a location where you will remember where to find it later. Once you have a location selected, you will want to create a new folder for your web pages. Click on the "New Folder" (1) Change the name of the new folder to something you like (2) and then Click the "Select Folder" button at the bottom (3)

![VSCode New Folder](images/vscode-new-folder.png?raw=true)


When you return to Code, you should have your new website folder open in your project.

![Code Folder](images/code-folder.png?raw=true)

Alright, now let's create a new file in your website folder for the text of our web page. We'll do this by hovering the mouse over the folder and clicking the icon that looks like a piece of paper with a plus sign (1).

![New file](images/new-file.png?raw=true)

Now, let's name the file "index.html". Really, you could call the page anything, but most websites have an index page as their first page, so it's a good idea to name your file this way.

Now, let's add some text to this file. Add a few lines like the following (or you can just cut and paste the following code to have enough text to follow along).

````Text
Visit Anytown, USA!

Things to Do
Hiking
Biking
Horseback
Backpacking

Amazing Museums
While most museums are a collection of old artifacts and stuff that no one is really interested in seeing, our musuems are the best of the best.
You won't find anything like these any where else in the world. Our museums rival that of our closest competitors including the Museum of Bad Art, the Paris Sewers Musuem and the Museum of Broken Relationships.
Come check them out...the fun is waiting for you.
 
SplashAnyone Waterpark
Our waterpark is the biggest and best park in the Western World. Just south of interstate 2015, you'll find a sweet mix of Super Slides and lazy rivers.
If that wasn't enough, we have 376 of the best food trucks in the state serving everything from fried gummy bears to lemonade and pizza. Don't forget if you buy our collectors edition souvenir water park keepsake, you get free refills all year.
And we wouldn't be SplashAnyone without the rules about splashing ... wait there are no rules.

Best Zoo in Town
Finally, you won't want to miss out cuddly little zoo animals. Lions, tigers and bears...Oh My! We have the largest selection of born in captivity animals. We didn't want to take the from their natural habitat, so we just got them from the other zoos in the state.

How to Get Here
By Plane
By Train
By Automobile
By Boat
````

So far, all we have is a little text. If we were to open that in a browser (go ahead and try it if you want to) you'll see something like this.

![Plain Text](images/plain-text.png?raw=true)

###Let's Add Some Formatting

> **Note:** Need to put in a explanation of HTML
HTML is a combination of a number of user interface concepts, and stands for Hyper-Text Markup Language.  Initially HTML was designed to facilitate professional collaboration in the high energy physcic community at CERN in 1989.  Use your browser to search for article on the history of the web beginning at CERN, there are many good resources.  Talk to your teacher or teaching assistant to learn more about the early history of the Internet.  
You might consider these questions:
<ul>
	<ol>Who is Tim Berners-Lee?</ol>
	<ol>What was the three new technologies that were incorporated into the HTML proposal?</ol>
	<ol>What was the Month and Year that the first information-sharing system using HTML, HTTP, and a client software program?</ol>
	<ol>What three letters are associated with the client software program for HTML?</ol>
<ul>


First, let's tell the browser that the document that we are working with is going to be an HTML document. We'll do that by putting the following code at the beginning of our file.

````HTML
<!doctype html>
Visit Anytown, USA!

Things to Do
Hiking
...
````

Most browsers will assume that it is HTML without this, but it's never a bad idea to set the expectation for the browser to view your file as HTML.

Next, we need to tell the browser where the HTML starts and stops. We do this by using tags. Opening tags look like this "\<html>" and closing tags look like this "\</html>". Let's put these at the top and bottom of your web page now.

````HTML
<!doctype html>
<html>
Visit Anytown, USA!

Things to Do
Hiking

...

By Automobile
By Boat
</html>
````

There are two parts of an HTML page. There is the \<head> which has some information that is descriptive of your page and then the \<body>. The \<body> is the content of your page and how it should be displayed.

Let's add those tags now. We don't have any \<head> content just yet, so we will just put in a blank set of tags. We'll come back and add more interesting stuff in a minute. The rest of the content we will surround with the \<body> tags.

````HTML
<!doctype html>
<html>
	<head></head>
	<body>Visit Anytown, USA!

Things to Do
...
By Automobile
By Boat
	</body>
</html>
````

Next, we want to set a number of the lines to be "header" lines. We do this with tags \<h1>, \<h2>, and so on to \<h6>. The top most level is \<h1>. While we are at it, we want to mark the paragraphs of text with a \<p> tag. This helps the browser to format these as individual paragraphs rather than creating one long block of text.

````HTML
<!doctype html>
<html>

<head></head>

<body>
	<h1>Visit Anytown, USA!</h1> 
	Things to Do 
	Hiking 
	Biking 
	Horseback 
	Backpacking

	<h2>Amazing Museums</h2>
	<p>While most museums are a collection of old artifacts and stuff that no one is really interested in seeing, our musuems are the best of the best.</p>
	<p>You won't find anything like these any where else in the world. Our museums rival that of our closest competitors including the Museum of Bad Art, the Paris Sewers Musuem and the Museum of Broken Relationships.</p>
	<p>Come check them out...the fun is waiting for you.</p>

	<h2>SplashAnyone Waterpark</h2>
	<p>Our waterpark is the biggest and best park in the Western World. Just south of interstate 2015, you'll find a sweet mix of Super Slides and lazy rivers.</p>
	<p>If that wasn't enough, we have 376 of the best food trucks in the state serving everything from fried gummy bears to lemonade and pizza. Don't forget if you buy our collectors edition souvenir water park keepsake, you get free refills all year.</p>
	<p>And we wouldn't be SplashAnyone without the rules about splashing ... wait there are no rules.</p>

	<h2>Best Zoo in Town</h2>
	<p>Finally, you won't want to miss out cuddly little zoo animals. Lions, tigers and bears...Oh My! We have the largest selection of born in captivity animals. We didn't want to take the from their natural habitat, so we just got them from the other zoos in the state.</p>

	How to Get Here 
	By Plane 
	By Train 
	By Automobile 
	By Boat
</body>

</html>
````

If you open your file in a browser now, it should look much nicer.

![H1 and P tags](images/h1-and-p-tags.png?raw=true)

Finally, we have two lists we want to work with. In HTML, we have two types of lists: Ordered and Unordered. An ordered list puts a numeric value at the beginning of each list item where unordered lists use a graphic symbol to mark each list item.

To create an ordered list, we use an \<ol> tag and for an unordered list, we use an \<ul> tag. For both lists, each individual list item is marked with an \<li> tag.

````HTML
	<h2>Things to Do<h2> 
	<ol>
		<li>Hiking</li>
		<li>Biking</li>
		<li>Horseback</li>
		<li>Backpacking</li>
	</ol>
````

````HTML
	<h2>How to Get Here</h2>
	<ul>
		<li>By Plane</li>
		<li>By Train</li>
		<li>By Automobile</li>
		<li>By Boat</li>
	</ul>
````

###Let's give your page a title
Remember that \<head> tag we put in early on. Let's go back and add another tag to tell your browser what to display in a window title. This will help us know which window is your web page.

This time we are going to insert a \<title> tag to the \<head>. There are other things we can put in the \<head> tag, but for now this is all we are going to do.

````HTML
<!doctype html>
<html>

<head>My First Web Page</head>

<body>
````

Congratulations, you turned a simple text file into an HTML file. You are now ready to move on and learn how to add some more style and flair to your web page.
