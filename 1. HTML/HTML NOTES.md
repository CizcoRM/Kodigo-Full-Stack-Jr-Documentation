# HTML

**What is HTML?**

HTML (HyperText Markup Language) is the standard language used to create and design documents on the World Wide Web. **HTML uses a system of tags and attributes** to define different parts of the document, making it possible to format and display content in a structured and visually appealing way.

**Basic estructure of a tag**
`<tag  attribute="value"> content </tag>`

**Attributes** determine specific information about the tag.

`<tag id="data" class="class1" lang="es">Content of the tag</TAG>`

Commentary ignores by we browser 

`<!-- This is a commentaty -->`

| Attribute | Value | Description |
| --- | --- | --- |
| id | name | Sets a unique identifier for the HTML tag. The same name can only be used once per document. |
| class | name | Sets a class (category) for an HTML tag. It can be repeated throughout the document. |
| style | CSS styles | Applies CSS properties directly to the specific HTML element. |

```html
<!-- DOCTYPE declaration for HTML5 -->
<!DOCTYPE html>

<!-- Root HTML element -->
<html lang="en">
  <!-- Head section containing metadata -->
  <head>
    <!-- Character encoding declaration -->
    <meta charset="UTF-8" />
    <!-- Viewport settings for responsive design -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!-- Title of the document -->
    <title>Document</title>
  </head>

  <!-- Body section containing the visible content -->
  <body>
    <!-- Header section -->
    <header>
      <!-- Main heading -->
      <h1>This is a title</h1>
    </header>

    <!-- Navigation section -->
    <nav>
      <!-- Unordered list for navigation menu -->
      <ul>
        <!-- List items for menu options -->
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>

    <!-- Main content section -->
    <main>
      <!-- Article section -->
      <article>
        <!-- Article heading -->
        <h2>Article Title</h2>
        <!-- Paragraph -->
        <p>This is a paragraph of text.</p>
      </article>

      <!-- Aside section for related content -->
      <aside>
        <!-- Aside heading -->
        <h3>Related Links</h3>
        <!-- Ordered list -->
        <ol>
          <!-- List items -->
          <li><a href="#">Link 1</a></li>
          <li><a href="#">Link 2</a></li>
        </ol>
      </aside>
    </main>

    <!-- Footer section -->
    <footer>
      <!-- Paragraph for copyright information -->
      <p>© 2024 Cizco Syntaxis for HTML. All rights reserved.</p>
    </footer>
  </body>
</html>

```

/GITHUB