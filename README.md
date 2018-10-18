# Atrium's intro to the world of coding

## Lesson 1

You are going to build this:

<img src="https://res.cloudinary.com/small-change/image/upload/v1537749507/Screen_Shot_2018-09-23_at_5.35.23_pm_wcdrnv.png" />

It will appear on your own computer i.e. no one else will be able to see it. 

At the end of Lesson 1 you should have a rough understanding of:

- What HTML, CSS and a server does.
- How to style a page.

### How does the internet work?

When you type `www.netflix.com/watch/80192018` into your browser, this shit happens:

<img src="https://res.cloudinary.com/small-change/image/upload/v1537751752/Screen_Shot_2018-09-23_at_6.14.45_pm_iasjdb.png" />

Lesson 1 will focus only on what the HTML looks like (step 3).

### Getting started on your laptop.

##### Install a text editor

You write:
- Written documents using Word
- Spreadsheets using excel
- Code documents using a text editor like <a href='https://www.sublimetext.com/3'>Sublime</a>

Download and install <a href='https://www.sublimetext.com/3'>Sublime</a>.

##### Make a project folder 
Make the following folders/files and open `lesson-01` using Sublime.
```
/apps
  /atrium-tech-talks
    /lesson-01
      index.html
```
### Writing your first chunk of HTML

Here's a basic layout:

```
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>My First Heading</h1>
    <p>My first paragraph.</p>
  </body>
</html>
```

Some of the most commonly used HTML tags are:

<img src="https://res.cloudinary.com/small-change/image/upload/v1537754698/Screen_Shot_2018-09-23_at_7.04.11_pm_gaeciz.png"/>

### Making your own webpage

##### Adding the correct text

Step 1: Add the correct text to the page. We'll use `h1` (most notable heading) for your name, and `h3`'s for your title and location.
```diff
<html>
  <head>
+    <title>Sam Henderson</title>
  </head>
  <body>
+    <h1>Sam Henderson</h1>
+    <h3>Engineer</h3>
+    <h3>San Franciso, California</h3>
  </body>
</html>
```

##### Adding pink/purple background

Step 2: Add the background color using CSS.

```diff
<html>
  <head>
    <title>Sam Henderson</title>
    <style>
+      .background {
+        position: fixed;
+        left: 0;
+        right: 0;
+        top: 0;
+        bottom: 0;
+        background-image: linear-gradient(261deg, #A2A8D2 1%, #DF6B96 100%);
+      }
    </style>
  </head>
  <body>
+    <div class="background">
      <h1>Sam Henderson</h1>
      <h3>Engineer</h3>
      <h3>San Franciso, California</h3>
+    </div>
  </body>
</html>
```

Your page should look like this:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538856932/Screen_Shot_2018-10-06_at_1.12.49_PM_ef4rxo.png" />

##### Making the text look nice.

Step 3: Make the font sans-serif, white, less bold and all the same size.

```diff
<html>
  <head>
    <title>Sam Henderson</title>
    <style>
+      body {
+        font-family: sans-serif;
+      }
      .background {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-image: linear-gradient(261deg, #A2A8D2 1%, #DF6B96 100%);
      }
+      .heading {
+        color: #fff;
+        font-size: 18px;
+        font-weight: 100;
+      }
    </style>
  </head>
  <body>
    <div class="background">
+      <h1 class="heading">Sam Henderson</h1>
+      <h3 class="heading">Engineer</h3>
+      <h3 class="heading">San Franciso, California</h3>
    </div>
  </body>
</html>
```
The text should now look like:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538857796/Screen_Shot_2018-10-06_at_1.28.45_PM_a3kv7x.png" />

##### Move the text into the middle.

Step 4: Let's move the text into the middle.

```diff
<html>
  <head>
    <title>Sam Henderson</title>
    <style>
      body {
        font-family: sans-serif;
      }
      .background {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-image: linear-gradient(261deg, #A2A8D2 1%, #DF6B96 100%);
      }
      .heading {
        color: #fff;
        font-size: 18px;
        font-weight: 100;
      }
+      .info-outer-container {
+        padding-top: 14vh;
+      }
+      .info-inner-container {
+        width: 100%;
+        max-width: 800px;
+        margin: 0 auto;
+      }
    </style>
  </head>
  <body>
    <div class="background">
+      <div class="info-outer-container">
+        <div class="info-inner-container">
          <h1 class='heading'>Sam Henderson</h1>
          <h3 class='heading'>Engineer</h3>
          <h3 class='heading'>San Franciso, California</h3>
+        </div>
+      </div>
    </div>
  </body>
</html>
```

Your text should now be centered:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538858083/Screen_Shot_2018-10-06_at_1.33.37_PM_muotpe.png" />

##### Add the Email button/link.

Step 5: Wack a button under the text and make it a link to open an email.

```diff
<html>
  <head>
    <title>Sam Henderson</title>
    <style>
      body {
        font-family: sans-serif;
      }
      .background {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-image: linear-gradient(261deg, #A2A8D2 1%, #DF6B96 100%);
      }
      .heading {
        color: #fff;
        font-size: 18px;
        font-weight: 100;
      }
      .info-outer-container {
        padding-top: 14vh;
      }
      .info-inner-container {
        width: 100%;
        max-width: 800px;
        margin: 0 auto;
      }
+      .email-btn {
+        background-color: white;
+        border-radius: 3px;
+        font-size: 18px;
+        border: none;
+        padding: 12px 48px;
+        margin-top: 24px;
+        color: #D7739E;
+      }
+      .email-btn:hover {
+        cursor: pointer;
+      }
    </style>
  </head>
  <body>
    <div class="background">
      <div class="info-outer-container">
        <div class="info-inner-container">
          <h1 class='heading'>Sam Henderson</h1>
          <h3 class='heading'>Engineer</h3>
          <h3 class='heading'>San Franciso, California</h3>
+          <a href="mailto:someone@yoursite.com?subject=Mail from website">
+            <button class="email-btn">Email Sam</button>
+          </a>  
        </div>
      </div>
    </div>
  </body>
</html>
```
You should now see this:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538858452/Screen_Shot_2018-10-06_at_1.39.53_PM_nwwaex.png" />

##### Add the rocks down the bottom of the page.

Step 6: Insert an image of the rocks and stick it to the bottom of the page.

```diff
<html>
  <head>
    <title>Sam Henderson</title>
    <style>
      body {
        font-family: sans-serif;
      }
      .background {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-image: linear-gradient(261deg, #A2A8D2 1%, #DF6B96 100%);
      }
      .heading {
        color: #fff;
        font-size: 18px;
        font-weight: 100;
      }
      .info-outer-container {
        padding-top: 14vh;
      }
      .info-inner-container {
        width: 100%;
        max-width: 800px;
        margin: 0 auto;
      }
      .email-btn {
        background-color: white;
        border-radius: 3px;
        font-size: 18px;
        border: none;
        padding: 12px 48px;
        margin-top: 24px;
        color: #D7739E;
      }
      .email-btn:hover {
        cursor: pointer;
      }
+      .rocks {
+        position: fixed;
+        bottom: 0;
+        width: 100%;
+      }
    </style>
  </head>
  <body>
    <div class="background">
      <div class="info-outer-container">
        <div class="info-inner-container">
          <h1 class='heading'>Sam Henderson</h1>
          <h3 class='heading'>Engineer</h3>
          <h3 class='heading'>San Franciso, California</h3>
          <a href="mailto:someone@yoursite.com?subject=Mail from website">
            <button class="email-btn">Email Sam</button>
          </a>  
        </div>
+        <img src="https://res.cloudinary.com/small-change/image/upload/v1537741706/rocks_heaeje.png" alt="Rocks" class="rocks">
      </div>
    </div>
  </body>
</html>
```
You should now see the rocks!

<img src="https://res.cloudinary.com/small-change/image/upload/v1538858872/Screen_Shot_2018-10-06_at_1.47.09_PM_urqagb.png" />

##### Add the sun

Step 6: Insert an image of the sun.

```diff
<html>
  <head>
    <title>Sam Henderson</title>
    <style>
      body {
        font-family: sans-serif;
      }
      .background {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-image: linear-gradient(261deg, #A2A8D2 1%, #DF6B96 100%);
      }
      .heading {
        color: #fff;
        font-size: 18px;
        font-weight: 100;
      }
      .info-outer-container {
        padding-top: 14vh;
      }
      .info-inner-container {
        width: 100%;
        max-width: 800px;
        margin: 0 auto;
      }
      .email-btn {
        background-color: white;
        border-radius: 3px;
        font-size: 18px;
        border: none;
        padding: 12px 48px;
        margin-top: 24px;
        color: #D7739E;
      }
      .email-btn:hover {
        cursor: pointer;
      }
      .rocks {
        position: fixed;
        bottom: 0;
        width: 100%;
      }
+      .sun-container {
+        position: fixed;
+        bottom: 0;
+        left: 0;
+        right: 0;
+        display: flex;
+        justify-content: center
+      }
+      .sun {
+        width: 100%;
+        max-width: 700px;
+        max-height: 280px;
+      }
    </style>
  </head>
  <body>
    <div class="background">
      <div class="info-outer-container">
        <div class="info-inner-container">
          <h1 class='heading'>Sam Henderson</h1>
          <h3 class='heading'>Engineer</h3>
          <h3 class='heading'>San Franciso, California</h3>
          <a href="mailto:someone@yoursite.com?subject=Mail from website">
            <button class="email-btn">Email Sam</button>
          </a>  
        </div>
+        <div class="sun-container">
+          <img src="https://res.cloudinary.com/small-change/image/upload/v1537741707/Semi_mkwky1.png" alt="Sun" class="sun">  
+        </div>
        <img src="https://res.cloudinary.com/small-change/image/upload/v1537741706/rocks_heaeje.png" alt="Rocks" class="rocks">
      </div>
    </div>
  </body>
</html>
```

You should now see the sun:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538859459/Screen_Shot_2018-10-06_at_1.56.55_PM_pusxlx.png" />


##### Separate CSS styling into it's own CSS file.

Step 7: Service some tech debt.

Make the following folder structure by adding `styles.css`

```diff
/apps
  /atrium-tech-talks
    /lesson-01
+      styles.css
      index.html
```

Now move all your CSS (code in the `<style></style>` tags) that is currently in `index.html`, into your new `styles.css` file.

Finally add:

```diff
+ <link rel="stylesheet" type="text/css" href="styles.css">
```
into your `<head></head>` tags. 

Your `index.html` should now look like:

```
<html>
  <head>
    <title>Sam Henderson</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
  </head>
  <body>
    <div class="background">
      <div class="info-outer-container">
        <div class="info-inner-container">
          <h1 class='heading'>Sam Henderson</h1>
          <h3 class='heading'>Engineer</h3>
          <h3 class='heading'>San Franciso, California</h3>
          <a href="mailto:someone@yoursite.com">
            <button class="email-btn">Email Sam</button>
          </a>  
        </div>
        <div class="sun-container">
          <img src="https://res.cloudinary.com/small-change/image/upload/v1537741707/Semi_mkwky1.png" alt="Sun" class="sun">  
        </div>
        <img src="https://res.cloudinary.com/small-change/image/upload/v1537741706/rocks_heaeje.png" alt="Rocks" class="rocks">
      </div>
    </div>
  </body>
</html>
```

### What have we learnt?

Firstly, you have made your first web page!

<img src="http://78.media.tumblr.com/tumblr_m5464bwVFv1qihztbo1_400.gif" />

You have: 
- written HTML (`index.html`) - the building blocks of the web
- styled the HTML using CSS (`styles.css`)
- learnt that when a browser like Chrome makes a request to a server, it responds with HTML. 

Server responding with HTML:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538860703/Screen_Shot_2018-10-06_at_2.17.53_PM_ukaecz.png" />


### What's in Lesson 2?

The internal monologue of the butler (server).
