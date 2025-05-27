# workshop
CRC workshop abesit
# HTML Cheat Sheet

## Table of Contents

1. [HTML Basics](#1-html-basics)
2. [HTML Document Structure](#2-html-document-structure)
3. [Text Elements](#3-text-elements)
4. [Links and Navigation](#4-links-and-navigation)
5. [Images and Media](#5-images-and-media)
6. [Tables](#6-tables)
7. [Forms](#7-forms)
8. [Semantic HTML5 Elements](#8-semantic-html5-elements)
9. [Containers and Layout](#9-containers-and-layout)
10. [HTML Attributes](#10-html-attributes)
11. [HTML Best Practices](#11-html-best-practices)
12. [HTML Quick Reference](#12-html-quick-reference)

# 1. HTML Basics

HTML (HyperText Markup Language) is the standard markup language used to create web pages. It describes the structure of a web page and consists of a series of elements that tell browsers how to display content.

## Document Structure
HTML documents follow a hierarchical structure. Every HTML document begins with a document type declaration, followed by the root HTML element that contains all other elements. The basic structure includes the head section for metadata and the body section for visible content.

## HTML Versions
HTML has evolved through several versions over the years. The current standard is HTML5, which introduced many new semantic elements, form controls, and multimedia capabilities. Previous versions include HTML 4.01, HTML 3.2, and earlier iterations. Each version brought improvements in functionality and standardization.

## DOCTYPE Declarations
The DOCTYPE declaration informs the browser about the version of HTML being used. For HTML5, the declaration is simple:
```html
<!DOCTYPE html>
```

For older HTML versions, the declarations were more complex and included references to Document Type Definitions (DTDs).

## HTML Comments
Comments in HTML are useful for documenting code and temporarily disabling content. They are not displayed in the browser. HTML comments are written as:
```html
<!-- This is a comment -->
<!-- 
    Multi-line
    comment
-->
```

## Character Entities
Character entities are used to display reserved characters in HTML or characters that are difficult to type. They begin with an ampersand (&) and end with a semicolon (;). Common examples include:

- `&lt;` for < (less than)
- `&gt;` for > (greater than)
- `&amp;` for & (ampersand)
- `&quot;` for " (quotation mark)
- `&apos;` for ' (apostrophe)
- `&nbsp;` for a non-breaking space

Numeric character references can also be used, either in decimal format (`&#169;` for Â©) or hexadecimal format (`&#x00A9;` for Â©).

# 2. HTML Document Structure

The structure of an HTML document follows a logical hierarchy that helps browsers interpret and render web content correctly. Understanding this structure is fundamental to creating well-formed HTML documents that display properly across different browsers and devices.

## HTML, HEAD, BODY Elements

Every HTML document consists of three main parts: the document type declaration, the head section, and the body section. The entire document is enclosed within the `<html>` root element, which typically includes a language attribute to specify the document's primary language.

The `<head>` element contains metadata about the document that isn't directly displayed on the page. This includes information like the document title, character encoding, viewport settings, and links to external resources such as stylesheets and scripts. The head section is crucial for SEO, browser rendering, and proper document interpretation.

The `<body>` element contains all the visible content of the webpage, including text, images, links, tables, forms, and other elements that users interact with. Everything that appears in the browser window is placed within the body tags.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Metadata goes here -->
</head>
<body>
    <!-- Visible content goes here -->
</body>
</html>
```

## Meta Tags

Meta tags provide additional information about the HTML document. They are placed within the `<head>` section and serve various purposes, from defining character encoding to improving SEO. Some essential meta tags include:

The character encoding declaration specifies how text is encoded in the document:
```html
<meta charset="UTF-8">
```

The viewport meta tag controls how the page is displayed on mobile devices:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Description and keyword meta tags help with search engine optimization:
```html
<meta name="description" content="A brief description of the page content">
<meta name="keywords" content="HTML, CSS, JavaScript, web development">
```

Author and copyright information:
```html
<meta name="author" content="Author Name">
<meta name="copyright" content="Copyright Owner">
```

## Title and Favicon

The document title appears in the browser tab and is important for bookmarking, history, and SEO. It is defined using the `<title>` element within the head section:
```html
<title>Page Title</title>
```

A favicon (favorite icon) is a small icon associated with a website that appears in browser tabs, bookmarks, and history. It is linked in the head section:
```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

Modern websites often include multiple favicon formats for different devices and platforms:
```html
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
```

## External Resources

HTML documents often link to external resources such as CSS stylesheets, JavaScript files, fonts, and more. These resources enhance the functionality and appearance of web pages.

CSS stylesheets are linked using the `<link>` element:
```html
<link rel="stylesheet" href="styles.css">
```

JavaScript files can be included using the `<script>` element, typically placed at the end of the body for better performance:
```html
<script src="script.js"></script>
```

Alternatively, JavaScript can be included in the head with the defer attribute:
```html
<script src="script.js" defer></script>
```

Web fonts can be linked directly or through services like Google Fonts:
```html
<link href="https://fonts.googleapis.com/css2?family=Open+Sans&display=swap" rel="stylesheet">
```

Preconnect and preload directives can optimize resource loading:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preload" href="important-image.jpg" as="image">
```


# 3. Text Elements

Text elements form the foundation of content presentation in HTML. They allow web developers to structure written content in a way that is both semantically meaningful and visually appealing. Understanding these elements is essential for creating well-organized and accessible web pages.

## Headings (h1-h6)

HTML provides six levels of headings, ranging from `<h1>` (the most important) to `<h6>` (the least important). Headings create a hierarchical structure for the document, helping both users and search engines understand the organization of content. The heading hierarchy should be maintained properly, with `<h1>` typically used for the main page title, and subsequent levels used for section and subsection headings.

```html
<h1>Main Page Title</h1>
<h2>Section Heading</h2>
<h3>Subsection Heading</h3>
<h4>Sub-subsection Heading</h4>
<h5>Minor Heading</h5>
<h6>Least Important Heading</h6>
```

Proper use of headings is crucial for accessibility, as screen readers use them to navigate through the document. Additionally, search engines give more weight to content in heading tags, particularly `<h1>` and `<h2>`, making them important for SEO.

## Paragraphs

The paragraph element `<p>` is used to group related sentences and create blocks of text. Browsers automatically add margin space before and after paragraphs, creating visual separation between text blocks. Paragraphs are the most common way to structure textual content on the web.

```html
<p>This is a paragraph of text. It can contain multiple sentences and will be displayed as a block-level element with margins above and below.</p>
```

While HTML ignores extra whitespace and line breaks in the source code, you can force a line break within a paragraph using the `<br>` element:

```html
<p>This text will appear on the first line.<br>This text will appear on the second line.</p>
```

## Text Formatting

HTML provides various elements for formatting text to emphasize or highlight certain parts. These elements add semantic meaning to the text rather than just visual styling, which should primarily be handled with CSS.

For strong emphasis, the `<strong>` element is used, which typically renders as bold text:
```html
<p>This is <strong>very important</strong> information.</p>
```

For regular emphasis, the `<em>` element is used, which typically renders as italic text:
```html
<p>This adds <em>subtle emphasis</em> to the text.</p>
```

Other text formatting elements include:

- `<mark>` for highlighted text: `<mark>Highlighted text</mark>`
- `<del>` for deleted text: `<del>Deleted text</del>`
- `<ins>` for inserted text: `<ins>Inserted text</ins>`
- `<sub>` for subscript: `H<sub>2</sub>O`
- `<sup>` for superscript: `2<sup>3</sup> equals 8`
- `<small>` for smaller text: `<small>Copyright notice</small>`
- `<code>` for inline code: `<code>var x = 10;</code>`
- `<pre>` for preformatted text that preserves spaces and line breaks

## Lists (ordered, unordered, definition)

HTML offers three types of lists for organizing information: ordered lists, unordered lists, and definition lists.

Ordered lists `<ol>` are used when the sequence of items matters. Each item is marked with a number or letter:
```html
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>
```

Ordered lists can be customized with attributes like `type` (for different numbering styles: 1, A, a, I, i) and `start` (to begin counting from a specific number).

Unordered lists `<ul>` are used when the sequence doesn't matter. Each item is typically marked with a bullet point:
```html
<ul>
    <li>Apples</li>
    <li>Oranges</li>
    <li>Bananas</li>
</ul>
```

Definition lists `<dl>` are used to display name-value pairs, such as terms and their definitions:
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language, the standard language for creating web pages.</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets, used for styling HTML documents.</dd>
</dl>
```

Lists can be nested within each other to create hierarchical structures, and list items can contain other HTML elements, not just text.

## Quotes and Citations

HTML provides specific elements for marking up quotations and citations, which helps maintain semantic meaning and can be useful for styling and accessibility.

The `<blockquote>` element is used for longer quotations that form a separate paragraph:
```html
<blockquote cite="https://source.com">
    <p>This is a longer quotation from an external source that forms its own paragraph.</p>
</blockquote>
```

For shorter, inline quotations, the `<q>` element is used:
```html
<p>As the saying goes, <q>To be or not to be, that is the question</q>.</p>
```

The `<cite>` element is used to reference the title of a work:
```html
<p>My favorite book is <cite>The Great Gatsby</cite> by F. Scott Fitzgerald.</p>
```

When combined, these elements provide proper semantic structure for quotations:
```html
<blockquote>
    <p>The only thing we have to fear is fear itself.</p>
    <footer>â€” <cite>Franklin D. Roosevelt</cite>, First Inaugural Address</footer>
</blockquote>
```

# 4. Links and Navigation

Links are fundamental to the web, allowing users to navigate between pages and resources. HTML provides robust mechanisms for creating various types of links that enhance user experience and website functionality.

## Anchor Tags

The anchor element `<a>` is used to create hyperlinks in HTML. It requires the `href` (hypertext reference) attribute to specify the link destination. The content between the opening and closing tags becomes the clickable text or element.

```html
<a href="https://www.example.com">Visit Example Website</a>
```

Anchor tags can link to external websites, internal pages, file downloads, specific sections within a page, email addresses, and telephone numbers. They form the backbone of web navigation and are essential for creating an interconnected browsing experience.

## Link Attributes

HTML links support various attributes that modify their behavior and appearance:

The `target` attribute determines where the linked document opens. Setting it to `_blank` opens the link in a new tab or window:
```html
<a href="https://www.example.com" target="_blank">Open in new tab</a>
```

Other target values include `_self` (default, opens in same frame), `_parent` (opens in parent frame), and `_top` (opens in full body of window).

The `rel` attribute specifies the relationship between the current document and the linked document:
```html
<a href="https://example.com" rel="nofollow">Example</a>
```

Common `rel` values include `nofollow` (tells search engines not to follow the link), `noopener` (prevents the new page from accessing the window.opener property), `noreferrer` (prevents passing the referrer information), and `external` (indicates the link leads to an external site).

The `title` attribute provides additional information about the link, typically displayed as a tooltip when hovering:
```html
<a href="https://example.com" title="Visit the Example website for more information">Example</a>
```

The `download` attribute suggests that the browser download the URL instead of navigating to it:
```html
<a href="document.pdf" download="filename.pdf">Download PDF</a>
```

## Internal Page Links

Internal links connect to different sections within the same webpage. They use the ID of the target element as the reference, preceded by a hash symbol (#):

First, add an ID to the target element:
```html
<h2 id="section-contact">Contact Us</h2>
```

Then, create a link to that section:
```html
<a href="#section-contact">Go to Contact Section</a>
```

These links are particularly useful for creating table of contents in long documents or for implementing single-page websites with smooth scrolling navigation.

To link to a specific section on another page, combine the page URL with the section ID:
```html
<a href="about.html#team">Meet Our Team</a>
```

## Email and Telephone Links

HTML provides special link types for initiating email composition and phone calls, which are especially useful for contact information.

Email links use the `mailto:` protocol in the href attribute:
```html
<a href="mailto:contact@example.com">Send us an email</a>
```

Email links can include additional parameters like subject, cc, bcc, and body:
```html
<a href="mailto:contact@example.com?subject=Inquiry&cc=info@example.com&body=Hello,">Contact with pre-filled email</a>
```

Telephone links use the `tel:` protocol, which is particularly useful for mobile browsing:
```html
<a href="tel:+1234567890">Call us at +1 (234) 567-890</a>
```

## Download Links

HTML allows you to create links that prompt the user to download a file rather than navigate to it. This is achieved using the `download` attribute:

```html
<a href="report.pdf" download>Download Report</a>
```

You can also specify a different filename for the downloaded file:
```html
<a href="report-v2.pdf" download="annual-report-2023.pdf">Download Annual Report</a>
```

For security reasons, the download attribute generally only works for same-origin URLs. When linking to files on different domains, the browser's behavior will depend on the Content-Disposition header sent by the server.

# 5. Images and Media

Images and media elements enhance web pages by providing visual and auditory content. HTML5 offers robust support for various media types, allowing developers to create rich, engaging experiences for users.

## Image Tags and Attributes

The `<img>` element is used to embed images in HTML documents. It is a self-closing tag that requires the `src` (source) attribute to specify the image file location:

```html
<img src="image.jpg" alt="Description of the image">
```

The `alt` attribute provides alternative text for the image, which is essential for accessibility. Screen readers read this text to visually impaired users, and it displays if the image fails to load. Writing descriptive alt text is a crucial accessibility practice:

```html
<img src="sunset.jpg" alt="Beautiful sunset over the ocean with orange and purple sky">
```

Images support several other important attributes:

The `width` and `height` attributes specify the dimensions of the image in pixels:
```html
<img src="logo.png" alt="Company Logo" width="200" height="100">
```

Setting these dimensions helps the browser allocate space for the image before it loads, reducing layout shifts and improving page performance.

The `loading` attribute can improve performance by deferring off-screen images:
```html
<img src="large-image.jpg" alt="Large landscape" loading="lazy">
```

The `srcset` and `sizes` attributes enable responsive images that adapt to different screen sizes and resolutions:
```html
<img src="photo.jpg" 
     srcset="photo-small.jpg 500w, photo-medium.jpg 1000w, photo-large.jpg 2000w" 
     sizes="(max-width: 600px) 500px, (max-width: 1200px) 1000px, 2000px" 
     alt="Responsive photo">
```

## Image Maps

Image maps allow different regions of an image to become clickable, with each region linking to a different destination. This is achieved using the `<map>` and `<area>` elements:

```html
<img src="world-map.jpg" alt="World Map" usemap="#worldmap">

<map name="worldmap">
    <area shape="rect" coords="0,0,200,200" href="north-america.html" alt="North America">
    <area shape="circle" coords="350,250,100" href="europe.html" alt="Europe">
    <area shape="poly" coords="450,300,500,320,480,350" href="asia.html" alt="Asia">
</map>
```

The `shape` attribute defines the shape of the clickable area (rectangle, circle, or polygon), while the `coords` attribute specifies the coordinates that define the area. The `href` attribute works just like in anchor tags, defining the link destination.

## Audio Elements

HTML5 introduced the `<audio>` element for embedding sound content without requiring plugins:

```html
<audio controls>
    <source src="music.mp3" type="audio/mpeg">
    <source src="music.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>
```

The `controls` attribute adds playback controls (play/pause, volume, seek bar). Multiple `<source>` elements can provide different audio formats for browser compatibility.

Additional audio attributes include:

- `autoplay`: Starts playing the audio automatically (often blocked by browsers)
- `loop`: Repeats the audio when it ends
- `muted`: Sets the initial state to muted
- `preload`: Suggests how the browser should preload the audio (none, metadata, auto)

```html
<audio controls autoplay loop muted preload="metadata">
    <source src="background-music.mp3" type="audio/mpeg">
</audio>
```

## Video Elements

The `<video>` element embeds video content in HTML documents:

```html
<video width="640" height="360" controls>
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.webm" type="video/webm">
    Your browser does not support the video tag.
</video>
```

Like the audio element, video supports multiple source formats for compatibility and includes the `controls` attribute for playback controls.

Other important video attributes include:

- `poster`: Specifies an image to show before the video plays
- `autoplay`, `loop`, `muted`, and `preload`: Function similarly to their audio counterparts
- `playsinline`: Allows videos to play inline on iOS (instead of fullscreen)

```html
<video width="640" height="360" controls poster="vid