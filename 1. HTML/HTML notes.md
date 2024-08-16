# HTML Basics

## Table of Contents

- [HTML Basics](#html-basics)
  - [Table of Contents](#table-of-contents)
  - [**What is HTML?**](#what-is-html)
  - [**Basic HTML structure**](#basic-html-structure)
  - [**Common Attributes**](#common-attributes)
    - [Identifier: The id attribute](#identifier-the-id-attribute)
    - [Classes: The class attribute](#classes-the-class-attribute)
    - [Inline Styles: The style attribute](#inline-styles-the-style-attribute)
  - [**- Other Attributes**](#--other-attributes)
  - [**- Obsolete Tags**](#--obsolete-tags)
  - [**HTML TAGS**](#html-tags)
    - [**`<head>` Document Header tags**](#head-document-header-tags)
      - [**The `<title>` tag**](#the-title-tag)
      - [**The `<meta>` tag**](#the-meta-tag)
      - [**Google Indexing Metadata**](#google-indexing-metadata)
      - [**The `<base>` tag**](#the-base-tag)
      - [The `<link>` tag](#the-link-tag)
      - [**Relationship with CSS styles**](#relationship-with-css-styles)
      - [**Aditional information or data**](#aditional-information-or-data)
      - [**Types of resources**](#types-of-resources)
    - [**HTML Grouping Tags**](#html-grouping-tags)
      - [**Main Content `<main>`**](#main-content-main)
      - [**Paragraph of text `<p>`**](#paragraph-of-text-p)
      - [**Thematic separation of the text `<hr>`**](#thematic-separation-of-the-text-hr)
      - [**Dividers `<div>`**](#dividers-div)
      - [**List of elements `<ul>` `<ol>`**](#list-of-elements-ul-ol)
      - [**Quotes and citations `<blockquote>`**](#quotes-and-citations-blockquote)
  
## **What is HTML?**

HTML (HyperText Markup Language) is the standard language used to create and design documents on the World Wide Web. **HTML uses a system of tags and attributes** to define different parts of the document, making it possible to format and display content in a structured and visually appealing way.

---

**Basic structure of an HTML tag**
`<tag attribute="value"> content </tag>`

- **Tags:** In HTML5 there's a specific set of predefined tags, these are enclosed within opening `<tag>` and closing tags `</tag>` .
- **Attributes** determine specific information about the tag. The value is always enclosed in **double quotes**.

    `<tag attribute="value"> content </tag>`

    There are 3 types of attributes:

    1. **Set of values**: These only allow specific values. Any other value will be invalid.
    2. **Free values**: These are attributes where you can freely specify a value, such as a URL or text.
    3. **Boolean values**: These are attributes that must have either a true or false value.
- **Tag content:** This is where you place the information you want to be affected by the tag.

    `<tag id="data" class="class1" lang="es">Content</tag>`

    A tag can have multiple attribute-value pairs. However, the same attribute should never be repeated within a single tag.

- **Commentary** ignored by the browser, used to explain and document the code.

    `<!-- This is a commentary -->`

## **Basic HTML structure**

The document structure is divided into **three parts.** **Document type `<**!DOCTYPE html>`. Then, we open the **`<html>`** tag that will contain two main parts: the document **header** **`<head>`** and the document **body** **`<body>`**.

``` HTML
<!DOCTYPE html>
<html lang="es">
 <head>
   <title>Títule</title>
   <meta charset="utf8">
 </head>
 <body>
   ...
 </body>
</html>
```

`<!DOCTYPE html>`  It must always be specified so that the browser knows what type of HTML document it is.

**`<head>`** is not a visual part of the web page, but a part of where certain metadata tags are included for good SEO.

**`<body>`** All the visual elements of a page are located inside the tag.

## **Common Attributes**

| Attribute | Value | Description |
| --- | --- | --- |
| id | name | Sets a unique identifier for the tag can only be used once per document. `<div id="unique-identifier">This is a div with an id</div>` |
| class | name | Sets a class for an HTML tag. It can be repeated throughout the document. `<p class="highlight important">This is a paragraph with classes</p>` |
| style | CSS styles | Applies CSS properties directly to the specific HTML element. `<span style="color: blue; font-weight: bold;">This is a span with inline style</span>` |

### Identifier: The id attribute

This is an identifier for an HTML tag and a way to give it a name.

- It must not start with a number, but can contain numbers later on.
- The text should be in `kebab-case`
- Without strange characters, accents, or emojis.
- There cannot be two elements with the same `id`.

`<div id="unique-identifier">This is a div with an id</div>`

They are used when we want to locate specific areas that we know will not be repeated on the same page. Unless it's necessary to identify a unique area on the page, it's best to avoid using `id`.

### Classes: The class attribute

There can be elements with the same class in a document and a tag can have multiple different classes separated by space, not necessarily a single one.

`<p class="highlight important">This is a paragraph with classes</p>`

### Inline Styles: The style attribute

It is used in HTML tags to embed CSS code directly in the tag itself. However, in most cases, it is not recommended to add the styles in this way but to place the CSS code in a separate `.css` document of our HTML document.

`<span style="color: blue; font-weight: bold;">This is a span with inline style</span>`

## **- Other Attributes**

| Metadata Attribute | Value | Description |
| --- | --- | --- |
| title  | message | Message displayed in a tooltip when moving the mouse over an element. `<p title="This is a tooltip">Hover over me to see the title tooltip</p>` |
| data-* | text | Metadata in the tag itself. Any name with data- para prefix containing information, usually oriented to be used from Javascript or CSS, can be used.. `<div data-user-id="123" data-role="admin">Custom data attributes</div>` |
| accesskey | shortcut | Key combination that can be pressed by the user to activate the element.`<a href="#" accesskey="h">Home (Press Alt + h)</a>` |
| lang | language | Indicates the language of the HTML tag content.`<p lang="es">Hola, ¿cómo estás?</p>` |
| translate | yes / no | Sets the directionality of the text. `<p translate="no">Do not translate this text</p>` |
| dir | ltr / rtl | Establece la direccionalidad del texto (left to right o right to left).`<p dir="rtl">This text will be right-to-left</p>` |

## **- Obsolete Tags**

| Obsolete Tag | Description | Alternative |
| --- | --- | --- |
| `<applet>` | Tag for Java applets. | Javascript, DOM and CSS |
| `<acronym>` | Indicates an acronym. | `<abbr>` |
| `<bgsound>` | Specifies a background sound. | `<audio>` |
| `<dir>` | Indicates a list of files or folders. | `<ul>` |
| `<frame>` | Defines a specific frame. | `<iframe>`  |
| `<isindex>` | Field to search in the document. | `<input>` |
| `<listing>`, `<xmp>` | Source code fragments. | `<pre>`,`<code>` |
| `<noembed>` | Alternative (fallback) for content. | `<object>`  |
| `<strike>` | Displays strikethrough text. | `<s>` |
|  `<basefont>` | Defines a default font. | CSS: font-family |
| `<big>` | Increases text size. | CSS: font-size |
| `<blink>` | Displays blinking text. | CSS: animation |
| `<center>` | Centers the text. | CSS: text-align |
| `<font>` | Changes the font or its characteristics. | CSS: font-family |
| `<marquee>` | Displays text moving from side to side. | CSS: animation |
| `<multicol>` | Multiple columns. | CSS: columns |
| `<nobr>` | Prevents text from line breaking. | CSS: white-space |
| `<spacer>` | Inserts a horizontal space. |   |
| `<tt>` | Displays text with a monospaced font. | `<code>` |

## **HTML TAGS**

### **`<head>` Document Header tags**

There are several tags that can be used in the `<head>` section of the HTML document.

| HTML Tag | Where can it be used? | Description |
|----------|------------------------|-------------|
| `<title>` | ✅ `<head>` ❌ `<body>` | Indicates the title of the page (browser tab or title in Google search results). |
| `<base>` | ✅ `<head>` ❌ `<body>` | Base URL for links (used to manage relative paths). |
| `<link>` | ✅ `<head>` ❌ `<body>` | Establishes a relationship between the current document and an external one. See link tag |
| `<meta>` | ✅ `<head>` ❌ `<body>` | Sets a specific metadata in the current document. See meta tag |
| `<style>` | ✅ `<head>` ✅ `<body>` | Creates CSS styles that will only affect the current document. |
| `<script>` | ✅ `<head>` ✅ `<body>` | Indicates a script to load or execute on the current page. |

#### **The `<title>` tag**

Inside the `<head>` tag, it is advisable to always include at least the following two tags:

```HTML
<head>
  <title>Títule</title>
  <meta charset="utf-8" />
</head>
```

Title tag can be use to:

- Determines the title of the browser window or tab.
- If the page is indexed by Google, it's likely to use this title for search results.
- It's an identifying title that can be used by bots or automated systems reading the page.

#### **The `<meta>` tag**

The `<meta>` tag is used in HTML to provide metadata about the document. Can include information such as character encoding, page description, keywords, author, and viewport settings for responsive design. This tag is crucial for search engine optimization (SEO) and proper rendering of web pages across different devices.

| Valor name | Valor content | Description |
|------------|---------------|-------------|
| description | text | Indicates the page description that appears in search engines. |
| keywords | keywords | List of keywords separated by commas. Google does not take it into account. |
| author | name | Indicates the name of the page author. |
| application-name | name | Indicates the name of the web application. Should only be used if it's a webapp. |
| generator | software | Indicates the software used to create the web page. |
| theme-color | color | Hexadecimal color of the navigation bar. |

```HTML
<head>
    <meta charset="UTF-8">  the way in which the text characters of a page are displayed.
    <meta name="description" content="This is an example of a meta description. This will often show up in search results.">
    <meta name="keywords" content="HTML, CSS, JavaScript, Web Development">
    <meta name="author" content="Guillermo Melendez">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="robots" content="index, follow">
</head>
```

#### **Google Indexing Metadata**

| Value name | Value content | Description |
|------------|---------------|-------------|
| google | nositelinkssearchbox | Tells Google not to display the mini search box in the sitelinks. |
| google | notranslate | Tells Google not to translate the page. |
| robots | parameters | Tells a search engine robot whether or not to index the page. |
| viewport | parameters | Behavior of the visible region of the browser. Responsive. |

| Parameters | Meaning |
|------------|---------|
| index | Suggests to Google that you want to index the content of the page in the search engine. |
| noindex | Tells Google not to index the content of the page in the search engine. |
| follow | Suggests to Google to follow the links found on the page. |
| nofollow | Tells Google not to follow the links found on the page. |
| nosnippet | Tells Google not to display snippets (description, etc...). |
| noodp | Tells Google not to use the alternative description from DMOZ. Currently obsolete. |
| noarchive | Tells Google not to store a cached version of the page. |
| unavailable_after date | Sets an expiration date for the page to no longer be crawled. |
| noimageindex | Tells Google not to index the page in Google Images results. |
| none | Equivalent to indicating the noindex, nofollow parameters. |

#### **The `<base>` tag**

The `<base>` tag can be used to establish a base path for relative links used in our document.

```HTML
<head>
  <title>HTML document using base</title>
  <base href="https://main/links/" target="_blank">
</head>
<body>
  <a href="index.html">Home page</a>
  <a href="./other_page/">Other page</a>
</body>
```

| Target Attrib | Description |
|-----------------|-------------|
| _self           | The link opens in the same tab. It's the default value, even if the attribute is omitted. |
| _blank          | The link opens in a new tab or window. |

#### The `<link>` tag

The `<link>` tag is used to establish relationships with other documents, links, or files.

| Rel attribute | Description |
|---------------|-------------|
| **Visual Information** ||
| stylesheet | Establishes a relationship with a .css document to apply its styles. |
| icon | Indicates an icon to use as a favicon (tab icon). |
| **Document** ||
| alternate | Indicates an alternative version of the current document. |
| pingback | Indicates a link that should be pinged when this document is referenced. |
| **SEO Positioning** ||
| canonical | Establishes the real link for the current document to avoid duplicate URLs. |
| prev | Indicates if there is a previous URL to the current document. Useful in multi-part links. |
| next | Indicates if there is a next URL to the current document. Useful in multi-part links. |
| **Information or Data** ||
| author | Indicates a link with more information about the author of the current document. |
| help | Indicates a link with help information. |
| search | Indicates a link where a search engine for the current site can be found. |
| license | Indicates a link with the license information for the current page. |
| manifest | Indicates a link with a URL to a .json file with an application manifest. |

| Resource Hints | Description |
|----------------|-------------|
| preload | Indicates resources that should be loaded as soon as possible. |
| prefetch | Indicates resources that may be needed for the next navigation. |
| preconnect | Indicates origins that will be connected to in the near future. |
| dns-prefetch | Indicates origins for which DNS lookups should be performed in advance. |

#### **Relationship with CSS styles**

The most widespread use is to establish a relationship with a CSS document.

```html
<head>
  <link rel="stylesheet" href="index.css">
</head>
```

#### **Aditional information or data**

```html
<head>
  <link rel="author" href="https://twitter.com/profile">
  <link rel="help" href="https://html.com/help/">
  <link rel="search" href="https://html.com/search/">
  <link rel="license" href="https://html.com/license/">
</head>
```

#### **Types of resources**

Attribute where you need to indicate the type of file to reference.

| Attribute | Description | Formats |
|----------------|-------------|---------|
| `document` | HTML document or links used in `<iframe>` elements. | .html |
| `script` | Javascript document. | .js |
| `audio` | Audio file that can be used in an `<audio>` element. | .mp3, .ogg, .opus, ... |
| `video` | Video file that can be used in a `<video>` element. | .mp4, .webm, ... |
| `image` | Image or graphic document that can be used in `<img>` or `<picture>`. | .jpg, .png, .webp, ... |
| `font` | Typography loaded using the CSS @font-face rule. | .woff2, .woff, .ttf |
| `style` | CSS style document. | .css |
| `track` | Subtitle file used in `<track>` elements. | .vtt |
| `fetch` | Link to which an XHR or fetch request is made. Requires the `crossorigin` attribute. | |

### **HTML Grouping Tags**

A tag that contains a group of tags related in some way. Although it is not mandatory to have a class, `<div>` tags are usually given a class for several reasons:

- To identify it as a specific section
- For visual styling (CSS)
- For functionality (Javascript)

| Tag | Description |
|-----|-------------|
| `<div>` | Layer or division used to group multiple HTML tags. |
| `<p>` | Defines a paragraph of text (with its HTML tags for text). |
| `<main>` | Container to encompass the main part of the page. |
| `<hr>` | Indicates a thematic separation of the text. |
| `<ol>` | Creates a numbered list (with order). |
| `<ul>` | Creates a list where order doesn't matter. |
| `<li>` | Contains one of the items of a numbered or unnumbered list. |
| `<pre>` | Establishes preformatted text (respecting spaces and line breaks). |
| `<blockquote>` | Groups information and characteristics of a quote (author, source, etc...). |
| `<dl>` | Creates a definition list. |
| `<dt>` | Establishes the term of a definition. |
| `<dd>` | Establishes the description of a term in a definition. |
| `<figure>` | Groups a visual element into a figure or illustration. |
| `<figcaption>` | Establishes a caption for a figure or illustration. |

``` html
<div class="container">
  <p>This is paragraph.</p>
  <p>This is a second paragraph.</p>
</div>
```
#### **Main Content `<main>`**

The HTML `<main>` tag is a tag that allows us to group all the main content of a page. In principle, an HTML document should only have one `<main>` tag.

```html
<body>
  <main>
    <p>Main content of the page.</p>
  </main>
  <aside>
    <p>Page information.</p>
  </aside>
</body>
```

There are situations where multiple `<main>` elements can exist. These situations imply that all `<main>` tags in the document have the `hidden` attribute defined except for one.

```html
<body>
  <main>
    <h1>Home page</h1>
  </main>
  <main hidden>
    <h1>Services</h1>
  </main>
  <main hidden>
    <h1>About me...</h1>
  </main>
</body>
```

#### **Paragraph of text `<p>`**

The HTML `<p>` tag is used to group paragraphs of text.

`<p>This would be a paragraph of text.</p>`

#### **Thematic separation of the text `<hr>`**

The HTML `<hr>` tag is used to indicate a thematic separation of the text to establish a separation between contents.

```html
<h2>Section 1</h2>
<p>This is the content of section 1.</p>
<hr>
<h2>Section 2</h2>
<p>This is the content of section 2.</p>
```

#### **Dividers `<div>`**

The `<div>` tag is a tag that is usually used to create a grouping of one or more tags and organize them in a specific division.

```html
<div class="container">
  <h2>This is a div example</h2>
  <p>The div tag is used to group content together.</p>
  <div class="container2">
    <ul>
      <li>It can contain multiple elements</li>
      <li>It's often used for styling purposes</li>
      <li>It's a block-level element</li>
    </ul>
  </div>
</div>
```

As much as possible, always try to avoid nesting HTML elements inside each other if it is not strictly necessary.

There are other sementic tags that can be used instead of `<div>`:

- `<section>`: Represents a section of a document.
- `<article>`: Represents a self-contained composition in a document, page, application, or site.
- `<header>`: Represents a container for introductory content or a set of navigational links.
- `<footer>`: Represents a footer for its nearest sectioning content or sectioning root element.
- `<aside>`: Represents a portion of a document whose content is only indirectly related to the document's main content.
- `<nav>`: Represents a section of a page that links to other pages or to parts within the page.
- `<main>`: Represents the main content of a document.
- `<figure>`: Represents self-contained content, potentially with an optional caption, which is specified using the `<figcaption>` element.

#### **List of elements `<ul>` `<ol>`**

If we need to make a list of items, we can use the `<ul>` tag for unordered lists and the `<ol>` tag for ordered lists. In both lists, we can use the `<li>` tag to define each item.

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>
```

#### **Quotes and citations `<blockquote>`**

The `<blockquote>` tag is used to indicate a quote or citation.

```html
<blockquote cite="https://example.com/quote">
  <p>This is a quote.</p>
</blockquote>
```
