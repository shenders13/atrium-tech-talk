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
```
<html>
  <head>
    <title>Sam Henderson</title>
  </head>
  <body>
    <h1>Sam Henderson</h1>
    <h3>Engineer</h3>
    <h3>San Franciso, California</h3>
  </body>
</html>
```

##### Adding pink/purple background

Step 2: Add the background color using CSS.

```
<html>
  <head>
    <title>Sam Henderson</title>
    <style>
      .background {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-image: linear-gradient(261deg, #A2A8D2 1%, #DF6B96 100%);
      }
    </style>
  </head>
  <body>
    <div class="background">
      <h1>Sam Henderson</h1>
      <h3>Engineer</h3>
      <h3>San Franciso, California</h3>
    </div>
  </body>
</html>
```

Your page should look like this:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538856932/Screen_Shot_2018-10-06_at_1.12.49_PM_ef4rxo.png" />

##### Making the text look nice.

Step 3: Make the font sans-serif, white, less bold and all the same size.

```
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
    </style>
  </head>
  <body>
    <div class="background">
      <h1 class="heading">Sam Henderson</h1>
      <h3 class="heading">Engineer</h3>
      <h3 class="heading">San Franciso, California</h3>
    </div>
  </body>
</html>
```
The text should now look like:

<img src="https://res.cloudinary.com/small-change/image/upload/v1538857796/Screen_Shot_2018-10-06_at_1.28.45_PM_a3kv7x.png" />
