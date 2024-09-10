# Introduction

Fronend refers to what you see in a web page, it talks about the structure and appearance of your website. Here you will learn:

- **HTML** stands for HyperText Markup Language and it allows to structure of Web Page.

- **CSS** stands for Cascading Style Sheets and it will comes for appearance, in other words, the color, sizes, locations and more.

One of your best friends during this selection will be the Inspection option in your web browser (Chrome, Firefox, Brave...), which can be accessed with **F12**:

![inspection_overview](/frontend_developer_course/resources/inspection_overview.png)

Also, before we start coding you will need to learn about the rendering engines, which is the tool inside the web browser that allows to convert the code to a form that understand the application and then display it in screen. Let's check some options:

- [Chrome](https://www.google.com/chrome/): [Blink](https://www.chromium.org/blink/)
- [Edge](https://www.microsoft.com/en-us/edge?ep=0&form=MA13FJ&es=40&ch=1): [Edge HTML](https://es.wikipedia.org/wiki/EdgeHTML)
- [Safari](https://www.apple.com/safari/): [Webkit](https://webkit.org/)
- [Firefox](https://www.mozilla.org/en-US/firefox/): [Gecko](https://firefox-source-docs.mozilla.org/overview/gecko.html)
- [Brave](https://brave.com/) : [Blink](https://www.chromium.org/blink/)

For more info on rendering engines, you can go and check this interesting blog from GeekForGeeks about [Rendering engines used by different Web Browsers?](https://www.geeksforgeeks.org/rendering-engines-used-by-different-web-browsers/)

Everyone make a list of steps to achieve the visualization you see usually in a Web Browser:

1. Convert the files into objects
2. Calculate the correspoding style to DOM node.
3. Calculate the dimensions of each node and the region where they go on screen.
4. Paint the different boxes and parts
5. Take all the lyers and convert them in a single image for the screen.

TODO: Add image of allegory of HTML/CSS 

# HTML:

## Brief comments on the usage of HTML:

The structure of HTML is composed of elements, for example:

```HTML
<h1> Learning HTML </h1>
```

Which is composed of:

- Opening tag: ```<h1>```
- Content: ```Learning HTML
- Closing tag: ```</h1>```

But the structure can also allow attributes and values:

```HTML
<h1 class = "title">
```

Which is composed of:

- Attribute: ```class```
- Value: ```"title"```

Another important thing to highlight, is that you can nest instructions:

```HTML
<section>
    <h1> Name </h1>
    <p> Paragraph </p>
    <ul>
        <li> Item </li>
    </ul>
</section>
```

And keep in mind that not every element will have opening and closing tags:

```HTML
<img src="image.jpg" alt="name_image"/>
```

## Anatomy of a HTML Document

Using the next structure:

```HTML
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title> Amazing title </title>
    </head>
    <body>
        <header>...
        <nav>...
        <section>...
        <footer>...
    </body>
</html>
```

Always keep present that_
- The ```DOCTYPE``` specifies that we are working with HTML.
- All the HTML code should be inside the ```<html>``` tags to be considered and avoid errors.
- **Head** is oriented for titles, fabicons and useful links for the documents.
- **Body** is for the structure of the HTML related to text, paragraphs and images.

To check our first example, you can go to the [index.html](/frontend_developer_course/practice/01_intro_to_html/index.html) file in the directory **01_intro_to_html** present in the practice directory that is where we will put the examples we do during the course.

Remeber that you can create files from the terminal by using the **touch** command:

```bash
touch <filename>
```

One trick that can save you a lot of time when using HTML, is to use the snippets or emmets, for example, if you have enabled the **HTML Extensions** in VS Code, you can add *HTML:5* and it will create a template for you.

![HTML5_emmet](/frontend_developer_course/resources/html_5_emmet.png)

## Semantic HTML

It refers to tags  with meaning, which allow your website to be more accessible, improve the SEO positioning and have a clearer code.

Remember that you have to use the proper tags, for example, do not use a ```<div>``` to create a header, and instaed use a ```<header>```.

## Most used tags

Let's make a brief overview of commonly used tags:

- **Layouts:** It talks about the general design and structure of the webpage.
    - ```<header>``` : For the start of the document.
    - ```<nav>``` : Navigation bar
    - ```<section>``` : Divide in sections.
    - ```<article>``` : Related to articles.
    - ```<aside>```
    - ```<footer>``` : For the last part.
- **Links:** For URLs and other link resources.
    - ```<a>``` : Links for redirection
- **Texts:** 
    - ```<h1>...<h6>``` : You can go from h1 up to h6, no more. It should related importance.
    - ```<p>``` : Paragraphs
    - ```<span>``` : Helps for formatting inside a paragraph.
- **Resources:** 
    - ```<img>``` : Add images.
    - ```<svg>``` : For vectorized images.
    - ```<ifram>e``` : For videos.
    - ```<video>``` : Also for videos
- **Forms:**
    - ```<form>``` : Forms
    - ```<input>``` : User input of different types.
    - ```<label>``` : Inital texto for what to do in the interaction.
    - ```<button>``` : For simple interaction of clic
- **Lists:**
    - ```<ul>``` : Specify a list encapsulation
    - ```<il>``` : Add item to list
    - ```<ol>``` : Ordered item.

For a more detailed and clearer reference, you can check the amazing guide offered by [htmlreference.io](https://htmlreference.io/).
