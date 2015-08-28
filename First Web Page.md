##Your First Web Page

###Let's just start with plain text
For now, we'll start with just a text file that will tell people a little about you, a school club or a hobby you like. We'll put this in our code editor even though we are just doing text.

Let's get going by starting up Visual Studio Code. Once the editor is open, we will want to start a new folder for all of our work. Start by click "File" (1) and the "Open folder..." (2)

![VSCode File Open Folder](images/vscode-file-open-folder.png?raw=true)

In the dialog window that comes up, navigate to a good location to store your new project. Often the best place will be your "Documents" folder, but choose a location where you will remember where to find it later. Once you have a location selected, you will want to create a new folder for your web pages. Click on the "New Folder" (1) Change the name of the new folder to something you like (2) and then Click the "Select Folder" button at the bottom (3)
[//]:# Comment:************ BEGIN *****************
[//]:# Comment: I would do a list here of what to do, but what is written is definitely a friendlier way to do it.
[//]:# Comment: No changes
[//]:# Comment:
[//]:# Comment:*************END********************

![VSCode New Folder](images/vscode-new-folder.png?raw=true)

When you return to Code, you should have your new website folder open in your project.

![Code Folder](images/code-folder.png?raw=true)
[//]: # Comment: ************ BEGIN *****************
[//]: # Comment: This image does not map to the outcome if I use the folder shown in image.  Recommend that the two should be the same.
[//]: # Comment: ************ END    *****************

Alright, now let's create a new file in your website folder for the text of our web page. We'll do this by hovering the mouse over the folder and clicking the icon that looks like a piece of paper with a plus sign (1).

(![New file](images/new-file.png?raw=true)

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
[//]:# Comment: ************ BEGIN *****************
[//]:# Comment: Although I would find Fried Gummy Bears interesting, why is this example so long?
[//]:# Comment: It is a good example, but it also adds a great deal of "words" to the explaination
[//]:# Comment: I would recommend that less words, say something like a club event would be a better way to go
[//]:# Comment: No change requested
[//]:# Comment: ************ END *****************

So far, all we have is a little text. If we were to open that in a browser (go ahead and try it if you want to) you'll see something like this.

![Plain Text](images/plain-text.png?raw=true)

[//]:# Comment: ************ BEGIN *****************
[//]:# Comment: Not in my browser, following the exact steps
[//]:# Comment: I did not save the index.html according to the instructions
[//]:# Comment: Also, how did I know how to open the index.html file?
[//]:# Comment: Might be a good idea to add the concept that the file size is important, it is zero before saving and about 2 kb after signing.
[//]:# Comment: ************ END *****************

###Let's Add Some Formatting

> **Note:** Need to put in a explanation of HTML
[//]:# Comment:************ BEGIN *****************
[//]:# Comment:
[//]:# Comment: ************ END *****************


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
[//]:# Comment: ******************************* START
[//]:# Comment: Why do I need to tell the HTML to start and stop?  Might too wordy to explain.  But for most people who use modern tools for editing this might be confusing.  For instance I do not have to tell Word where to start and stop.  Again, just a thought. 
[//]:# Comment: Why is there a wrench on the left hand side of the tag?
[//]:# Comment: ****************************** END
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
[//]:# Comment:************ BEGIN *****************
[//]:# Comment: Why didn't my "Visit Anytown, USA!" tab over, do I tab it over?
[//]:# Comment: ************ END *****************

Things to Do
...
By Automobile
By Boat
	</body>
</html>
````

Next, we want to set a number of the lines to be "header" lines. We do this with tags \<h1>, \<h2>, and so on to \<h6>. The top most level is \<h1>. While we are at it, we want to mark the paragraphs of text with a \<p> tag. This helps the browser to format these as individual paragraphs rather than creating one long block of text.
[//]:# Comment:
[//]:# Comment: Define "header" lines?  Not a show stopper but I bet there will be some teachers who would like to answer that question.  For example:
"These tags create lines that are referred to as header lines because they are part of a class of elements that are called Metadata.  Metadata is not shown to the person who is reading the page."
[//]:# Comment:
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
[//]:# Comment: ************ BEGIN **************
[//]:# Comment: No it doesn't.  Need to make sure that they save the file
[//]:# Comment:************ END *****************

![H1 and P tags](images/h1-and-p-tags.png?raw=true)

[//]:# Comment: ************ BEGIN **************
[//]:# Comment:********* JUST A THOUGHT *********
[//]:# Comment: Why are lists important, bear in mind HS students might not understand why people like lists.  I like lists.
[//]:# Comment:************ END ***********************

Finally, we have two lists we want to work with. In HTML, we have two types of lists: Ordered and Unordered. An ordered list puts a numeric value at the beginning of each list item where unordered lists use a graphic symbol to mark each list item.
[//]:# Comment: ************ BEGIN **************
[//]:# Comment:********* JUST A THOUGHT *********
[//]:# Comment: Why did you use the term "numeric", it is in the vocabulary of the HS Student for sure, but... Why not just say number?  
[//]:# Comment:************ END ***********************
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
[//]:# Comment: ************ BEGIN **************
[//]:# Comment:********* JUST A THOUGHT *********
[//]:# Comment: Why not check out the page at this point?
[//]:# Comment:************ END ***********************

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

[//]:# Comment: ************ BEGIN **************
[//]:# Comment:
[//]:# Comment: Good job, the only fixes would the third image, make sure to remind them to save, explain HTML.
[//]:# Comment:************ END ***********************
