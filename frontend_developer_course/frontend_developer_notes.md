# Introduction

Fronend refers to what you see in a web page, it talks about the structure and appearance of your website. Here you will learn:

- **HTML** stands for HyperText Markup Language and it allows to structure of Web Page.

- **CSS** stands for Cascading Style Sheets and it will comes for appearance, in other words, the color, sizes, locations and more.

One of your best friends during these lessons will be the Inspection option in your web browser (Chrome, Firefox, Brave...), which can be accessed with **F12**:

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

When thinking about web programming, you can remember the next image to relate HTML, CSS and JS:

![Comparison HTML/CSS/JS](https://media.licdn.com/dms/image/v2/D5612AQGvsUSedZ4U3g/article-inline_image-shrink_1000_1488/article-inline_image-shrink_1000_1488/0/1705513570360?e=1731542400&v=beta&t=ym3PFCpBO16Z4m6BHPD3RYlJAcWhJ4rXgdq6dcXbNBE)


NOTE: All the codes presented here can be used for experimentation and illustration of the topics mentioned, to watch the result open the files in your web browser by pasing the absolute path to the file of interest:

```
file:///home/<user>/<path>/<to>/<repo>/frontend_developer_course/practice/16_metric_units_in_css/metric_units.html
```

All the codes presented were tested in the [Brave Browser](https://brave.com/), but they will work in other web browsers.

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

# CSS:

## Brief notes on CSS usage:

The basic structure is presented below:

```CSS
h1 {
    color : green;
}
```

In the previous example, we have to keep in mind the next:

- ```h1``` : It is the selector, it allows the communication with HTML, by specifying which part to give format
- ```{}```: It is where the CSS Code goes to format the specified element.
- ```color: ``` : In this case, it is a property.
- ```green;``` : It corresponds to a property's value.

## Anatomy of a selector:

### Basic Selectors:

First, let's mention the basic selectors, which are:

- **Of type:** ```div{...}``` -> Allows style of HTML tags.
- **Of class:** ```.element{...}``` -> Centered on objects from certain classes.
- **Of ID:** ```#element_id``` -> For editing the elements with the corresponding ID.
- **Of attribute:** ```a[href=""]{...}``` -> Modifications related to an attribute.
- **Universal:** ```*{...}``` -> Warning, modify everything.

You can check an example of this inside the file [selectors_p1.html](/frontend_developer_course/practice/04_intro_to_selectors_in_css/basis_selectors.html) inside the directory of the practice four, the CSS code is located inside the ```<style>``` tags.

If you want to explore what colors you can use, you can go to the [HTML Color Codes](https://htmlcolorcodes.com/)

### Combination selectors:

Another type of selectors are the ones for combination, which are:

- **Descendent:** ```div p```
- **Direct child:** ```div > p```
- **Adjacent element:** ```div + p```
- **General of brothers:** ```div ~ p ```

The usage of them, is shown in the file [selectos_p2.html](/frontend_developer_course/practice/05_combinator_selectors_css/comb_selectors.html) in the forlder of the practice number five.

## Pseudoclass and pseudoelements selectors:

They related with the actions an user make with the web site, for example, clic to a button, let's mention some of them:

- **Pseudoclass:**
    - ```:active``` : For active buttons
    - ```:hover``` : Related with mouse operations over images, text and buttons.
    - ```:nth-child(n)``` : Allow access for HTML elements.
    - ```:foucs``` : 
- **Pseudoelements:**
    - ```::after``` : Add something after a certain element, for example, an emoticon.
    - ```::before``` : Add something before a certain element, for example, an emoji or a text.
    - ```::first-letter``` For style of the first letter of praragraphs or related.
    - ```::placeholder``` : For text manipulation.

For examples, on this, go and check the [pseudo_selectors](/frontend_developer_course/practice/06_pseudo_selectors_in_css/pseudo_selectors.html) file in the practice number 6.

## Cascade and specificity:

The order of the rules matters, you should follow the cascade to determinate the output of the formatting. Also, sometimes, the web browser may not understand some rules you apply, therefore, you should be specific in the selectors you are using.

How to know which selector is more specific and important? Well, consider the next rules in the order from high priority to low priority.

1. ! Important. (x0000 value)
2. Line styles. (x000 value)
3. Id number. (x00 value)
4. Classes, attributes and pseudoclasses. (x0 value)
5. Elements and pseudoelements. (x value)
6. Universal selector. (0 value)

Considering the previous information, if we have the next declaration:

```CSS
#id h1::first-letter
...
#p .sidemenu div:hover
```

In one hand, it would mean that we have a value of 100 (id) + 1 (h1) + 1 (::first-letter) to result in 102 and, on the other hand, we would have a value of 1 (p) + 10 (.sidemenu) + 1 (div) + (:hover) to result in 22. Therefore, the first one is more specific.

If the previous paragraph, sound like poetry to you, yoo should check the practice 7 with the file [cascades.html](/frontend_developer_course/practice/07_cascades_in_css/cascades.html).

## Display types:

It refers for the visualization type of the HTML elements, it can be in **block**, **inline**, **inline-block**, **flex** and **grid**.

Do not forget to check which command support inline or block, with the [HTML-Reference](https://htmlreference.io/).

You can check an example about block, inline and block-inline in the code [block_inlines.html](/frontend_developer_course/practice/08_block_inlines_in_css/blocks_inlines.html) in the directory of the practice 8.

In the case of flex you can watch a brief example in the file [flex.html](/frontend_developer_course/practice/09_flex_css/flex.html) in the practice 9 directory. If you want to learn more, you can consider going to the [CSS Flexbox Layout Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) by CSS Tricks.

In the case of grid, you can watch a frief example in the file [grid.html](/frontend_developer_course/practice/10_grid_css/grid.html) in the practice 10 directory. If you are curious about them, you can learn more in [CSS Grid Layout Guide](https://css-tricks.com/snippets/css/complete-guide-grid/) by CSS Tricks.

## The Box Model:

When using **F12** with your web browser, have you checked the boxes display in the style part:

![box_example](/frontend_developer_course/resources/box_model_example.png)

Well, as you have watched, when we have CSS elements, they are mostly represented by boxes, those boxes has different properties which are **content**, **padding**, **border** and **margin**.

Try checking out this properties with a text in your HTML file, for example:

![content of awesom title](/frontend_developer_course/resources/box_model_content.png)
![margin of awesom title](/frontend_developer_course/resources/box_model_margin.png)

For more experimentation, you can go to the file [boxes.html](/frontend_developer_course/practice/11_boxes_in_css/boxes.html) and play in the web browser.

Keep in mind that when we have margin for adjacent blocks, they may overlap. However when we use flexbox, grid and element that aren't blocks, the margins won't overlap, you can check the example (and do not forget to interact with **F12**) in the case of the code [margins.html](/frontend_developer_course/practice/12_margins_in_css/margins.html).

## Positioning:

for a better display, you do not want to always display adjacent elements, in those cases you can position your content in relative, absolute, fixed, sticky, static, initial and inherital way.

You can watch an edxample with some of them in the [positioning.html](/frontend_developer_course/practice/13_positioning_css/positioning.html) file, of the practice 13. In this case, you may need to expermient a lot to understand them better.

### Z Index: 

Another important positioning is related with the fictional axis taht points to you, according to layers that may pose over, for example, commercials or logins. 

Originally, when you define the HTML, you create a layer order, but you can edit the **z-index** property for certain position types for improving the leayer distribution in your web page.

Here you should also consider the nested structures and parent structures, as initially a child cannot overlap its parent.

Go and checkout the example [z_index.html](/frontend_developer_course/practice/14_z_index_in_css/z_index.html) to learn and experiment more about the **z-index**.

## Most common properties in CSS:

Let's present a summary about what we have done with CSS, which are:

- **Layout:** Desgin orientations.
    - **Display:** For types of display box, inline, block-inline, grid and flex.
- **Text:** 
    - **font-size:** Letter size.
    - **font-weight:** Letter thickness.
    - **font-family:** Type of letter
    - **text-align:** Left, right, center, justified...
    - **color:** To add your style
- **Box Model:**
    - **margin:** External margin.
    - **padding:** Intern margin for content
    - **border:** Related with border color, size, thickness and style properties.
- **Background:**
    - **background:** For unified applied brackground color.
    - **background-color:** Another alternative for setting up the color.
- **Size:** 
    - **width:** In pixels.
    - **height:** In pixels. 

## Measure units:

How does the web browser knows the size of the elements? During the practices we have made, we have focused on using just pixels and percentage of the screen, but there are more.

They can be:

- **Absolute:** They do not depend on others, like pixels (*px*), (*pt*), (*pc*), inches (*in*), centimeters (*cm*), milimeters (*mm*).
- **Relative:** They depend on the screen/tab or relatateds *rem*, *em*, *vw* (view width), *vh* (view height), *vmin*, *vmax*, *ex*, *ch*.

To check the most used ones, go to the [metric_units.html](/frontend_developer_course/practice/16_metric_units_in_css/metric_units.html) file of the practice 16 and explore the sizes used.

## Responsive design:

This topic is related in how to make a website look fine in multiple platforms, for example, PC, tablet and smartphone.

We can do this with Media Queries, that follow the next structure:

```CSS
@media (max-width:375px){
    .class {
        update: value
    }
}
```

Go to the file [responsive.html](/frontend_developer_course/practice/17_responsive_design_in_css/responsive.html) and experimentate with the size of the screen, also, you can (in the inspection mode with F12) change the pixel size of your screen if you do not want to do it with the cursor.
