# FRApps
Step 1
From VSCode
Be certain that you have check "Auto Save" in the File menu
And that you have added "Live Server" to the "Extensions"

In a folder called BasicTrainig, create 2 new files.
    - index.html
    - index.css

Paste in the "favicon.gif" into the root directory.
    Thia will give you a nice FormR icon on the tab of your browser

Open the index.html and paste the following on Line 1:

HTML
``` 
1 <!DOCTYPE html>
2 <html lang="en">
3     <head>
4         <meta charset="UTF-8">
5         <meta http-equiv="X-UA-Compatible" content="ie=edge">
6         <link rel="stylesheet" href="index.css">
7         <link rel="shortcut icon" href="../favicon.gif">
8         <link href="https://fonts.googleapis.com/css?family=Bookman Old Style" rel="stylesheet">
9       <title>Basic-Training</title>
10     </head>
11    <body>
12        <div class="header">
13            <h2>header</h2>
14        </div>
15        <div class="section1">
16           <h2>section 1</h2>
17        </div>
18        <div class="section2">
19            <h1 class="descriptive-text">BASIC TRAINING</h1>
20            <h2>section 2</h2>
21        </div>
22        <div class="footer">
23            <h2>footer</h2>
24        </div>
25    </body>
26 </html>
```
Save this page, if you have NOT checked the "Auto Save" option in the File menu.

From VSCode, right click on the file "index,html" and click on "Open In Live Server"
    (This option will not be available if you had not added the "Live Server" extension)

You will see in your browser the following:

![](BasicImage1.jpg)
___

Open the index.css file and paste the following on Line 1

CSS
```
@import url('https://fonts.googleapis.com/css?family=Bookman Old Style');

html {
    background: #b3b3b3;
    height: 100%;
    text-align: center;
}

body {
    background: white;
    height: 100%;
}

.header {
    border: 1px solid red;
    background: red;
    color: white;
    width: 300px;
    height: 100px;
    position: relative;
}

.section1 {
    border: 1px solid blue;
    background: blue;
    color: white;
    width: 300px;
    height: 100px;
    position: relative;
}

.section2 {
    border: 1px solid lightgray;
    background: lightgray;
    color: black;
    width: 300px;
    height: 100px;
    position: relative;
}

.footer {
    border: 1px solid green;
    background: green;
    color: white;
    width: 300px;
    height: 100px;
    position: relative;
}

.descriptive-text {
    font-size: 20px;
    color: red;
    text-align: center;
}

.descriptive-text a:hover,
.descriptive-text a:active {
    color: green;
}
```

Congratulations, you have just created a simple html page with a cascading style sheet that makes 4 basic blocks!
This should be visible

To understand this lets look at the header css properties.

.header {                       CLASS NAME
    border: 1px solid red;          puts a 1 pixel red border around the block
    background: red;                makes the background red
    color: white;                   makes the font color white
    width: 300px;                   makes the block 300 pixels wide
    height: 100px;                  makes the block 100 pixels tall
    position: relative;             places the box relative to the html code - reading from the top to the bottom
}

We will be building from this basic page to create a page with fixed header and footer, links and a button and an image,

===========================================================

Next we will add to the code to the index.css file to continue building on our basic web page.

BODY

In the .body section add [ width: 100%;    /*this will open up the body to a 100% width*/ ]
to the bottom of the existing code WITHOUT the [brackets], like this:

body {
    background: white;
    height: 100%;
    width: 100%;    /*this will open up the body to a 100% width*/
    border:  1px solid black;
    margin: 0;
}
===========================================================
HEADER

In the .header section change width to 100% and height to 90px, like this:
    width: 100%;    /*was 300px*/
    height: 90px;   /*was 100px*/

.header {
    border: 1px solid black;
    background: red;
    color: white;
    width: 100%;    /*was 300px*/
    height: 90px;   /*was 100px*/
    position: relative;
}
===========================================================
SECTION1 & SECTION2

In section1 and section2, change the width to 100% and height to 380px:
    width: 100%;    /*was 300px*/
    height: 380px;  /*was 100px*/


===========================================================
FOOTER

In the .footer section change width to 100% and height to 90px, like this:
    width: 100%;    /*was 300px*/
    height: 90px;   /*was 100px*/

===========================================================
DESCRIPTIVE-TEXT

In the descriptive-text section, change the font-size to 25px, like this:
    font-size: 25px;

Add a top margin at the bottom:
    margin-top: 100px;
===========================================================
Congratulation, now look at your web page.  All the blocks now have changed to fill up the page
in Chrome.

===========================================================
Next we will add to the code to the index.css file to continue building on our basic web page to
include a FIXED header.

First, in the index.html file, replace:
    <h2>header</h2>
with:
    <span class="header-logo">My Logo</span>
this should be on line 13 in your VSCode.

Next let's work on the index.css file.  We will make additions to the .header properties and create some
new properties.

In the .header properties change the position from relative to fixed and add z-index: 100, like this:
    position: fixed;   /*was relative*/
    z-index: 100;
Now when scroll up and down the header is fixed, with "My Logo" centered at the top.

To make this look correct we have more work to do in the index.css file.
Below the z-index and these lines of code:

    display: flex;
    justify-content: space-between;

To get the logo to look good, add this code below the .header properties:

    .header-logo {
      font-family: "Bookman Old Style", sans-serif;
      font-size: 30px;
      font-weight: bolder;
      color: blue;
      text-shadow: 2px 2px 12px #000000;
      padding-left: 20px;
    }

    .header-logo::first-letter {
        font-size: 150%;
        color: cornflowerblue;
    }
You have a logo that is font-based.  Later we will change to an image.

To make all the blocks have their respective height and place on the page add:
    top: 92px;
at the bottom of ,section1 and .section2 and .footer--it should look like this for those three areas:

    .section1 {
        border: 1px solid blue;
        background: blue;
        color: white;
        width: 100%;    /*was 300px*/
        height: 382px;  /*was 100px*/
        position: relative;
        top: 92px
    }

    .section2 {
        border: 1px solid lightgray;
        background: lightgray;
        color: black;
        width: 100%;    /*was 300px*/
        height: 382px;  /*was 100px*/
        position: relative;
        top: 92px;
    }

    .footer {
        border: 1px solid green;
        background: green;
        color: white;
        width: 100%;    /*was 300px*/
        height: 90px;   /*was 100px*/
        position: relative;
        top: 92px;
    }

Next we will add some links and button to the header.

In index.html add the following code, just below the <span class="header-logo">My Logo</span>:
        <ul class="nav-list">
            <li class="nav-list-item"><a href=#>Links</a>&nbsp;&nbsp;&nbsp;</li>
            <li class="nav-list-item"><a href=#>Cards</a>&nbsp;&nbsp;&nbsp;</li>
            <li class="nav-list-item"><a href=#>FAQs</a>&nbsp;&nbsp;&nbsp;</li>
            <li class="nav-list-item-cta"><a href=#>Sign In</a></li>
        </ul>
This should start on line 14 in your VSCode.


...to be continued