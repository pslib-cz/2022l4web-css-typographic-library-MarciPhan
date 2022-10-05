## Grace.css - Free typography library

> Author: Adam Šáfr
Description

Maestro is a free typography CSS library. It was created for a school project. You don't need to make new CSS file every time you start new project. Maestro helps you style your headlines, special text markups, images, lists, basic tables, buttons, alerts and more. It's responsible and cross-browser friendly.
Demo site

There is link to demo site for style preview.
Content of the documentation

    Implementation
    Colours
    Typography
    Types of text
    Quotes
    Lists
        Unordered list
        Ordered list
    Table
    Alerts
    Buttons
    Pictures
    Code blocks
    Sections
    End

Implementation

    Download maestro.css in docs/download folder
    Add file inside your project folder
    Link maestro.css file to <head> in every HTML page using syntax:

<link href="maestro.css" rel="stylesheet">

Colours

Maestro.css has predefined colours. Between lines 3-31 you can find the list of colours. Selector :root defines colours for normal website mode. Selector [data-theme="dark"] defines the colours for website in dark mode. You can change them whatever you want.
Typography

Website font depends on your system. If you have an Apple device, the text will use Apple system font. Otherwise it will use Segoe UI and Roboto.
Headings

You can use headings from <h1> to <h6>. Font sizes are:

    30px for <h1>
    23px for <h2>
    20px for <h3>
    19px for <h4>
    18px for <h5>
    17px for <h5>

Types of text

Font size of normal text is 1rem. Other tags you can use are:

    <b> or <strong> for bold text
    <i> or <em> for italic text
    <u> for underlined text
    <s> for striked text

You can use special classes:

    class="all-caps" for CAPS text
    class="bold" for bold text
    class="small" for small text (size is 0.85 of normal text)

Quotes

For one line quote text use tag <q>. For multiple line text use <figure> with <blockquote>. It displays author name under the quote block. Syntax:

<figure>
    <blockquote>
        <p>Main quote text</p>
        <figcaption><span class="author">Author name</span>Work</figcaption>
    </blockquote>
</figure>

Lists

There are two types of lists:
Unordered list

The <ul> tag defines an unordered list. Use the <ul> tag together with the <li> tag to create unordered lists. Syntax:

<ul>
    <li>Item</li>
    <li>Item 2
        <ul>
            <li>More of item 2</li>
            <li>More of item 2</li>
        </ul>
    </li>
</ul>

Ordered list

The <ol> tag defines an ordered list. An ordered list is numerical. The <li> tag is used to define each list item. Syntax:

<ol>
    <li>First item</li>
    <li>Second item
        <ol>
            <li>Second item detail</li>
            <li>Second item detail</li>
        </ol>
    </li>
</ol>

Table

A table in HTML consists of table cells inside rows and columns. Each table cell is defined by a <td> and a </td> tag. Everything between <td> and </td> is the content of the table cell. Table head is defined by <thead> tag and has another background colour. Syntax:

<table>
    <thead>
        <tr>
            <th>Table heading 1</th>
            <th>Table heading 2</th>
            <th>Table heading 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Item 1</th>
            <th>Item 1</th>
            <th>Item 1</th>
        </tr>
        <tr>
            <th>Item 2</th>
            <th>Item 2</th>
            <th>Item 2</th>
        </tr>
        <tr>
            <th>Item 3</th>
            <th>Item 3</th>
            <th>Item 3</th>
        </tr>
    </tbody>
</table>

Alerts

There are 3 types of alert messages. Every message has same HTML structure but has different CSS class.

<div class="message message--warning">
    <span class="btn-close" onclick="this.parentElement.style.display='none';">x</span>
    <p>This is a warning alert box that will disappear when you click on X button.</p>
</div>

    Use class="message--warning" for warning alert.
    Use class="message--succes" for positive alert.
    Use class="message--basic" for normal alert.

Buttons

The <button> tag defines a clickable button. You can also use class="button" for any text tag with same effect. Example:

<button class="button">Text</button>
<input class="button" type="submit" value="Text">

There are 4 different classes for buttons:

    Use class class="btn-primary" for main button.
    Use class class="btn-noclick" for unclickable button.
    Use class class="btn-disabled" for no-effect button.
    Use class class="btn-warning" for danger button.

Pictures

The <img> tag is used to embed an image in an HTML page. Use this syntax for single image:

<figure class="gallery__block">
    <a href="./img/file.jpg">
        <img src="./img/file.jpg" alt="alternative text">
        <figcaption class="gallery__caption">Caption</figcaption>
    </a>
</figure>

Use this syntax for photo gallery. You can add as many <figure> into <div class="gallery"> as you want:

<div class="gallery">
    <figure class="gallery__block">
        <a href="./img/file.jpg">
            <img src="./img/file.jpg" alt="alternative text">
            <figcaption class="gallery__caption">Caption</figcaption>
        </a>
    </figure>
    <figure class="gallery__block">
        <a href="./img/file.jpg">
            <img src="./img/file.jpg" alt="alternative text">
            <figcaption class="gallery__caption">Caption</figcaption>
        </a>
    </figure>
</div>

Code blocks

The <pre> tag is used for indicating preformatted text. The <code> tag surrounds the code being marked up. Syntax:

<div class="code-block">
    <div class="pre-wrapper line">
        <pre><span class="code-tag">h1,</span>
        <span class="code-class">.text-h1</span><span class="code-punctuation"> {</span>
        <span class="code-text"><span class="code-punctuation">font-weight:</span> 500;
        <span class="code-punctuation">font-size:</span> 42px;
        <span class="code-punctuation">margin:</span> 0px 0px 0.7em 0px;</span>
        <span class="code-punctuation">}</span></pre>
    </div>
    <div class="pre-wrapper line">
        <pre><span class="code-punctuation">&lt;p </span><span class="code-class">class="text-h1"</span><span class="code-punctuation">&gt;</span> Heading <span class="code-punctuation">&lt;/p&gt;</span></pre>
    </div>
</div>

There are classes for highliting the code parts. Use them on <span> inside <pre> tag:

    Use class class="code-tag" for code tags.
    Use class class="code-class" for classes.
    Use class class="code-text" for normal texts.
    Use class class="code-punctuation" for code punctuations.

Sections

Inside <body> create <main> tag where you put sections <section>. Every <section> should have <h>tag inside. Then do whatever you want.
The end

I hope this CSS file will help you
Have a nice day 👍 🎉