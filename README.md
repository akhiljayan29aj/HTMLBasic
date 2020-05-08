# HOW TO USE THIS HTML SANDBOX

Just go through the above codes serial wise and refer this readme section for notes. I am using Visual Studio Code as my editor.

## 01. BASIC LAYOUT

Tag Syntax:
- Elements surrounded in angle brackets.
- Usually they have a starting and an ending tag.
- Some tags close themselves

Eg.
```
<!-- This is a HTML comment -->
<!-- START AND END TAG -->
<h1>Hello</h1>
<!-- SELF CLOSING TAGS -->
<br>  <!-- This is a line breaker -->
```

Now the basic layout :
```
<!DOCTYPE html>   <!-- This is the declaration of the type(in this case HTML5) -->
<html>  <!-- Parent Tag -->
  <head>  <!-- Child of HTML tag -->
    <title>My Website</title> <!-- This is the TITLE tag the text here appears in the title bar of the browser -->
  </head> 
  <body>  <!-- Child of HTML tag -->
    <!--This is a comment.-->
    <h1>My Website</h1> <!-- This is a HEADING tag -->
    <p>This is my very first website.</p>  <!-- This is a PARAGRAPH tag -->  
  </body>
</html>
```
## 02. Using Live Server

Live Server is a very handy tool which helps us to launch a local development server with live reload feature for static & dynamic pages.
You can simply install Live Server from the [VSCode Market Place](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).

## 03. META Tags

Meta tags are snippets of text that describe a page's content. They don't appear on the page itself, but only in the page's source code. Meta tags are essentially little content descriptors that help tell search engines what a web page is about.
Eg.

```
<meta charset="UTF-8">
```
This is a meta tag with a charset attribute. This defines the character set as UTF-8(This is the deafault if we remove this tag, the character set will still be UTF-8 which is the character & coding for unicode).

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
This meta tag is important for having a responsive design and using media queries.
```
<meta http-equiv="X-UA-Compatible" content="ie=edge">
```
This meta tag is used to set browser compatibilty.
```
<meta name="description" content="This is the description of my website.">
```
This meta tag will display the content in the description in the search engine results.
```
<meta name="keywords" content="web development, web design">
```
This meta tag contains the keywords which will help in search engine optimisation.
```
<meta name="robots" content="NOINDEX, NOFOLLOW">
```
This meta tag is used when we want that the website should not rank or show up in the search engine.


## 04. Typography

- HEADING

There are 6 HEADING tags h1 to h6, h1 being the biggest and h6 being the smallest.


- PARAGRAPH

  - p tag is used for making paragraphs.
  - strong tag makes the text bold.
  - em tag makes the text italic.
  - br tag is used to make a line break as simply using enter to make a line break in the p tag doesn't work.
  - hr tag breaks the line and also puts a horizontal line.
  - del tag strikes through the text.

## 05. Links and Images

- EXTERNAL LINK
```
 <a href="http://google.com">Click for GOOGLE</a>
```
This will generate a text GOOGLE which will be linked to "http://google.com". But this will link will be opened in the current tab not a new one. So, we will use an attribut target="_blank" to make the link open in a new tab.

- INTERNAL LINK
```
<a href="./04_typography.html">Typography</a>
```
This will open the typography.html file which is in the current folder. "./" means current folder and "../" means previous folder.

- LOCAL IMAGES
```
<img src="/images/sample.jpg" alt="sample image">
```
This will add an image of its full size and we need to resize the image using CSS.
The "scr" attribute contains the location of the image on the local machine.
The "alt" attribut contains alternative text which will be shown if the image doesnot load up.

- REMOTE IMAGES
```
<img src="https://source.unsplash.com/1600x900/?buildings" alt="My image">
```
To load a remote image we just need to change the "scr" attributes address to the address of the remote image.
[Unsplash Source](https://source.unsplash.com/) is a great site for image sharing.







 







