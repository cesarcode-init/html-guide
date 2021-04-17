# HTML Crash Course

### HTML sub-guide

- [HTML](#html)
- [HTML skeleton](#html-skeleton)
- [Headings](#headings)
- [Paragraphs](#paragraphs)
- [Anchors](#anchors)
- [Media](#media)
- [Lists](#lists)
- [Attributes](#attributes)
- [Links](#links)
- [Meta](#meta)
- [Semantics](#semantics)
- [Non-semantics](#non-semantics)
- [Styles](#styles)
- [Tables](#tables)
- [iframes](#iframes)
- [Forms](#forms)
- [Buttons](#buttons)
- [Select](#select)
- [Datalist](#datalist)
- [Template](#template)
- [SVGs](#svg)
- [Comments](#Comments)

This crash course targets beginners in web development. It helps and guides those who want to have a thorough understanding of HTML tags. It can also be a refresher for advanced developers.

### HTML

So What's HTML?
HTML is a **Hypertext Markup Language**. It is not ~~a programming language~~; it's just a way of structuring the content and rendering it on a webpage. To use this markup language, you will have to employ HTML _opening tags <>_ and _closing tags </>_.
So what do you have to learn in HTML? You need to understand the basics.

Note that when you create a new file you have to save it with an `.html` extension. For instance, the homepage is conventionally named `index.html`.

[back to sub-guide](#html-sub-guide)

### HTML Skeleton

HTML skeleton triggers the environment where you are going to work. Before starting any projects, you will have to include the following HTML skeleton:

```html
<!-- `DOCTYPE html` refers to the declaration of the HTML version you are using which is basically HTML5. -->

<!DOCTYPE html>
<html>
  <head>
    <!-- We use <meta> tags to add data that characterises a webpage. -->

    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- <title> tag allows you to add the website's name. -->
    <title>Webpage</title>

    <!-- <link> tag lets you add stylesheets where you can add styles to the webpage. -->
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <!-- Inside the <body> tag, we add all that has to do with the webpage content. -->
  </body>
</html>
```

[back to sub-guide](#html-sub-guide)

### Headings

Headings are titles that go from `<h1>`, the biggest, to `<h2>`, the smallest.

```html
<h1>I am a title</h1>
<h2>I am a title</h2>
<h3>I am a title</h3>
<h4>I am a title</h4>
<h5>I am a title</h5>
<h6>I am a title</h6>
```

[back to sub-guide](#html-sub-guide)

### Paragraphs

We use `<p>` tags to declare paragraphs.

```html
<p>I am a paragraph.</p>
```

[back to sub-guide](#html-sub-guide)

### Anchors

We use `<a>` tags to create hyperlinks that take the user to another page other than the current one or navigate in the same page.

```html
<a href="http://www.google.com">Visit Google</a>
```

[back to sub-guide](#html-sub-guide)

### Media

1. Images

We use `<img>` tags to add images. Note that these tags are _self-closing_ tags which means they don't require a closing tag; it closes itself.

```html
<img src="apple.jpg" alt="apple" />
```

`src` and `alt` attributes are required. `src` contains the image path. `alt` contains a brief phrase about that image so in case the internet breaks down somehow, the user will still know what the image is.

2. Videos

We use `<video>` tags to insert videos.

```html
<video controls>
  <source src="olaf.mp4" type="video/mp4" />
</video>

<!-- video tags can have multiple attributes to give the videos some functionalities like:
    
        1. 'controls' to make the video controllable by the user.
        2. 'muted' to make the video in silent mode.
        3. 'autoplay' as the attribute suggests to make the video play when a webpage first loads
        4. 'poster='thumbnail.jpg' to place a poster before the video kicks off.
-->
```

3. Audios

We use `<audio>` tags to insert audios.

```html
<audio controls>
  <source src="olaf.mp3" type="audio/mpeg" />
</audio>

<!-- audio tags can have multiple attributes to give the audios some functionalities like:
    
        1. 'controls' to make the audio controllable by the user.
        2. 'muted' to make the audio in silent mode.
        3. 'autoplay' as the attribute suggests to make the audio play when a webpage first loads.
-->
```

[back to sub-guide](#html-sub-guide)

### Lists

1. Ordered Lists

Ordered lists are number based lists. They go in a chronological order.

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```

2. Unordered Lists

Unordered lists are bullet point based. They are not organised in a chronological order.

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

3. Definition Lists

Definition lists are description based lists. They contain a description and terms attached to it.

```html
<dl>
  <dt>Item 1</dt>
  <dd>Item 1 is an amazing product which you can buy</dd>
  <dt>Item 2</dt>
  <dd>Item 2 is a fantastic product</dd>
</dl>
```

[back to sub-guide](#html-sub-guide)

### Attributes

1. Ids

We use an `id` attribute when an element has a unique style that's not common.

```html
<p id="unique">
  <!-- Note that you can give any other name. It doesn't have to be 'unique', it can be a name of your choice such as 'text', 'danger' etc. -->

  I have an id attribute. You can only select me because I'm unique.
</p>
```

2. Classes

We use a `class` attribute when some elements share common styles. We can also reference single elements.

```html
<p class="red-text">
  I have a class. That doesn't make me special. Other tags and I have a common
  class because we share common styles.
</p>

<p class="red-text">
  I'm another tag which shares the same style with my neighbour tag
</p>
```

3. Hyper-reference

We use `<a>` tags to create a hyperlink. To make it work, we need to insert the link inside the attribute `href`, which stands for hyper-reference.

```html
<a href="http://www.domain.com"
  >I have got a hyper-reference (href) on me so you can go to that link</a
>
```

4. Source (src)

We use the `src` attribute to add the image path.

```html
<img src="cat.png" />
```

5. Alternative (alt)

`alt` plays the role of an alternative for images not being displayed due to connection problems. It shows up the phrase you include inside the `alt` attribute.

```html
<img src="cat.png" alt="this is a cat" />
```

6. Style

We use the attribute `style` to add some styles to the elements.

```html
<p style="color: red;">I'm a paragraph and my color is red</p>

<!-- Note that there are three ways of adding styles to our webpage:
        1. Inline style which is achieved through using the attribute style.
        2. Style tag inside the head tag.
        3. Separate stylesheets.
 -->
```

7. Title

The `title` attribute gives a brief description of elements being hovered on. For instance, when a user hovers over a logo, a text shows up displaying 'Home'.

```html
<a href="http://www.youtube.com" title="go to YouTube">YouTube</a>
```

[back to sub-guide](#html-sub-guide)

### Links

Let's agree on something. This `link` is not like the hyperlinks enclosed by `<a>` tags. We add this `link` tag inside the `head` as it contains stylesheets.

```html
<link rel="stylesheet" href="style.css" />
```

[back to sub-guide](#html-sub-guide)

### Meta

`<meta>` tags contain special data about a webpage

```html
<meta charset="UTF-8" />
```

[back to sub-guide](#html-sub-guide)

### Semantics

1. Header

`<header>` tags always come at the top of the webpage inside the `<body>` tag. It's like an opening that usually contains a logo, a navigation menu, a search bar etc., depending on the projects.

```html
<header>
  <p>Hello I am a paragraph inside a header.</p>
</header>
```

2. Main

`<main>` tags appear between the headers and footers inside the `<body>` tag. They usually contain the centre or essentials of the webpage such as sections, articles, figures etc.

```html
<main>
  <p>Hello I am a paragraph inside a main.</p>
</main>
```

3. Footer

`<footer>` tags appear at the end of a webpage. They usually play the role of the ending. They contain contact information, navigation links and copyright statements.

```html
<footer>
  <p>Hello I am a paragraph inside a footer.</p>
</footer>
```

4. Navigation

`<nav>` tags are shorthand versions of _navigation_. We use them when we want to add a navigation bar.

```html
<nav>
  <a href="index.html">home</a>
  <a href="about.html">about</a>
  <a href="contact.html">contact</a>
</nav>
```

5. Sections

`<section>` tags are used to structure our content in a better way. A webpage can have multiple sections; each section tackles a specific area.

```html
<section>
  <p>I'm inside a section</p>
</section>
```

6. Articles

`<article>` tags are used for self-contained content such as a blog post etc.

```html
<article>
  <p>I'm inside an article tag</p>
</article>
```

7. Asides

`<aside>` tags are used to display parts of the content and they are often presented as _sidebars_.

```html
<aside>
  <p>
    I'm inside an aside tag. You will find me on the right or left side of the
    webpage
  </p>
</aside>
```

8. Figures

`<figure>` tags are handy when we want to insert an image or a document that has a caption under it.

```html
<figure>
  <img src="parrot.jpg" alt="this is a parrot picture" />
  <figcaption>Fig1. - Red Parrot.</figcaption>
</figure>
```

9. Blockquotes

`<blockquote>` tags are meant to wrap quotes.

```html
<blockquote cite="http://en.wikipedia.org/wiki/Main_Page">
  I'm a quote taken from a wikipedia page.
</blockquote>
```

[back to sub-guide](#html-sub-guide)

### Non-semantics

1. Spans

`<span>` tags are a quick way to grab the content inside it and give it a unique style with CSS or functionality with JavaScript.

```html
<span>I'm inside a span which makes me an inline element</span>
```

2. Divs

`<div>` tags are important when we want to control children etc.

```html
<div>I'm inside a div (division) which makes me a block element</div>
```

[back to sub-guide](#html-sub-guide)

### Styles

`<style>` tag is a way to add styles to our webpage by selecting the elements from HTML and styling them. We usually place this tag inside the `<head>` tag.

```html
<style>
  p {
    color: red;
  }
</style>
```

[back to sub-guide](#html-sub-guide)

### Tables

`<table>` tags are meant to create tables on a webpage.

```html
<table>
  <tr>
    <th>first name</th>
    <th>last name</th>
  </tr>
  <tr>
    <td>Brad</td>
    <td>Smith</td>
  </tr>
</table>
```

[back to sub-guide](#html-sub-guide)

### Iframes

`<iframe>` tags are used to embed another document within the current HTML document.

```html
<iframe src="demo.html" title="this is an Iframe"></iframe>
```

[back to sub-guide](#html-sub-guide)

### Forms

1. Form Tag

`<form>` tag is meant to declare a form. Forms are important to get data from users. There are various types of forms such as sign-in, sign-up, contact forms etc.

```html
<form action="#" method="POST">
  <!-- Here where form elements have to be -->
</form>
```

2. Form Elements

```html
<form action="#" method="POST">
  <!-- A label tag acts like a title -->
  <label>First name:</label>

  <!-- Inputs -->
  <!-- Inputs act like a placeholder where you can insert some data. -->

  <!-- Inputs with a type of text are designed to have text in them. -->
  <input type="text" />

  <!-- Inputs with a type of password are designed to have passwords in them that are hidden. -->
  <input type="password" />

  <!-- Inputs with a type of radio display a radio button which allows you to select one of the multiple choices. -->
  <input type="radio" />

  <!-- Inputs with a type of checkbox display a checkbox button which allows you to select one zero or more than one choice. -->
  <input type="checkbox" />

  <!-- Inputs with a type of submit display a submit button that allows you to submit the form -- it technically comes at the end of the form. -->
  <input type="submit" />

  <!-- Inputs with a type of button display a clickable button that allows you to click. -->
  <input type="button" />
</form>
```

3. Form Attributes

`action` attribute is designed to take care of the data submitted. It is the endpoint where the data is captured. Once the user fills in the data and presses on submit, you will have to create a server path where the data goes and be dealt with on the server-side.

```html
<form action="#" method="POST"></form>
```

`method` attribute determines the HTTP method you want to apply before the data is sent to the server. These methods are POST, GET, DELETE etc.

[back to sub-guide](#html-sub-guide)

### Buttons

1. Button Tag

`<button>` tags are meant to create clickable buttons.

```html
<button type="button">click me</button>
```

2. Button Input

`<input>` tags with a type of button are also meant to create a clickable button.

```html
<input type="button" value="click me" />
```

`value` attribute allows the button to have a description.

[back to sub-guide](#html-sub-guide)

### Select

`<select>` tags are meant to create a dropdown list with options. The user has to choose one of the options.

```html
<select>
  <option value="red">Red</option>
  <option value="blue">Blue</option>
  <option value="black">Black</option>
</select>
```

[back to sub-guide](#html-sub-guide)

### Datalist

`<datalist>` tags allow you to create a dropdown list with options like `<select>` tags; however, the difference is that `<datalist>` tags allow users to add their own options if they are not okay with the recommended ones.

```html
<datalist>
  <option value="red"></option>
  <option value="blue"></option>
  <option value="black"></option>
</datalist>
```

`value`, as it may seem, attribute adds a value to the options. There is another way to it, excluding the `value` attribute:

```html
<datalist>
  <option>red</option>
  <option>blue</option>
  <option>black</option>
</datalist>
```

[back to sub-guide](#html-sub-guide)

### Template

`<template>` tags are used to hide data and manipulate it using JavaScript to display it.

```html
<template>
  <p>I'm hidden inside this template till a user click to display me</p>
</template>
```

[back to sub-guide](#html-sub-guide)

### SVG

`<svg>` tags are used to create SVGs.

```html
<svg>
  <rect height='100' width='100' style='fill: red;'>
</svg>
```

[back to sub-guide](#html-sub-guide)

### Comments

```html
<!-- This is a comment in HTML -->
<!-- Comments don't show up on a webpage -->
```

Thank you for your attention. I hope this course has been as informative as you expected. There is more to it, but covering every bit of HTML would distracting. I have picked up the most important tags which you will end up using sooner or later.

For more, follow me on Instagram [@cesarcode.init](https://www.instagram.com/cesarcode.init/)
