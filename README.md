# HOW TO USE THIS HTML SANDBOX

Just go through the above codes serial wise and refer this readme section for notes. I am using Visual Studio Code as my editor.

## 01. Basic Layout

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

## 06. List and Tables

- Unordered List

ul tag is used to create an unordered list.

li tag is used create an list item inside the list.


- Ordered List

ol tag is used to create an ordered list.

- Nested List

We can also nest these lists.

- Tables

table tag is used to create a table. It has 2 children tags:

1. thead tag: This is used to create the head of the table. This has a child tag, tr tag which stands for table row. This is used to create a table row. Now this tr tag contains th tag which will add columns to the row.

2. tbody tag: This is used to create the body of the table. This has a child tag, tr tag which stands for table row. This is used to create a table row. Now this tr tag contains td tag which will add columns to the row.

## 07. Forms and Inputs

```
<form action="process.php">
```
The form tag is used to create a form. The action atrribute is where the form will be submitted.

In this file a div tag is used. This tag is used to create different divisions within the markup for easy access and seperation.

- For Text
```
<label for="name">Name</label><br>
```
This is a inline element therefore we need to use br tag to put the next element to the next line.

"for" attribute needs to match the id of the input. This will add the functionality that if we click on the Name it will highlight the corresponding input box.
```
<input type="text" id="name" name="name" placeholder="Enter your name">
```
"type" attribute sets the type of input.

"name" attribute is used on the server side.

"placeholder" attribute will hold the given value in the input field till the user hasn't given any input. This is not actual text, just a shodow can be over wriiten without deleting.

- For Email
```
<label for="email">Email</label><br>
<input type="email" name="email" id="email" value="@gmail.com">
```
"value" attribute  will prefill this input with @gmail.com.

- For Textarea
```
<label for="message">Message</label><br>
<textarea name="message" id="message" cols="30" rows="10"></textarea>
```
The "col" and "row" attributes will provide the character space. In this case, it will provide a 30x10 space.

- For Select
```
<label for="gender">Gender</label><br>
<select name="gender" id="gender">
  <option value="male">Male</option>
  <option value="female" selected>Female</option>
  <option value="other">Other</option>
</select>
```
The select tag will create a drop down menu which will contain the options made using the option tag.

The "selected" attribute will pre-select the option.

- For number
```
<label for="age">Age</label><br>
<input type="number" name="age" id="age">
```

- For Date
```
<label for="birthdate">Birthdate</label><br>
<input type="date" name="birthdate" id="birthdate">
```

- For Radio
```
<label for="membership">Membership</label>
<input type="radio" name="membership" id="membership" value="simple">Simple
<input type="radio" name="membership" id="membership" value="standard" checked>Standard
<input type="radio" name="membership" id="membership" value="super">Super
```
The input tag will only create selectors.

We need to label them after the input tag ends. In this case "Simple" is the label for the first selector.

We can use "checked" attribute to make the input pre-selected.

- For checkbox
```
<label for="vehicles">I like..</label>
<input type="checkbox" name="vehicles" id="vehicles" value="bike">Bike
<input type="checkbox" name="vehicles" id="vehicles" value="car">Car
<input type="checkbox" name="vehicles" id="vehicles" value="boat" checked>Boat
```
"value" attribute holds the data that is sent to the server.

###### NOTE:
1. select tag will create a drop down menu with option tags as input.
2. type="radio" makes selectors. In radio we can only select one input at a time.
3. type="checkbox" makes selectors too but we can select multiple at a time.

- Input Submit and Reset
```
<input type="submit" value="Submit"><br>
<input type="reset" value="Reset"><br>
```
"value" attribute holds the Text to bhi displayed.

- Button Submit and Reset
```
<button type="submit">Submit</button> 
<button type="reset">Reset</button>
```

## 08. Inline VS Block Level Element

Block level elements span across 100% of the width therefore the next thing will be knocked over to the next line.

Inline level elements doesn't span across the width, it only takes up that space and the next thing will go to the right of the element

## 09. Div, span, id and class

div and span are functionally same but the difference is that span is an inline element whereas div is a block level element.

We should treat id as a unique thing to a div or an element and classes can be used multiple times in different divs or elements.

## 10. Entities

There are some entities reserved in HTML5. This is because use of these may disturb the markup. So, we can use the entities in the above files.

## 11. Semantic Tags

These tags can be used as a replacement of divs for different section of the structure of the page.

- header tag : This tag usually go at the top. It has the logo. It may have the navigation and search box.
- nav tag : This is for the navigation. It has an unordered list. It can be a side menu.
- main tag : This is for the main content of the page.
- section tag : The main tag can contain different section tags.
- article tag : The section tag can contain different article tags.
- aside tag : This is for the sidebar content. This is not the main focus of the page. It can contain ADs or categories section.
- footer tag : This goes at the bottom. It contains copyright statements

![Basic Structure of a webpage using Semantic tags](https://www.w3schools.com/html/img_sem_elements.gif)
 







