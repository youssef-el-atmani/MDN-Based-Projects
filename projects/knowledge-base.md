# Knowledge Base

> Here I'll store all the knowledge starting from the date `27 Feb 2025`\
> That knowledge is strictly related to `web dev`, and mostly related to `Front End Dev`\
> Also the knowledge that will be listed here is strictly practical, theoretical one will have its own file\

## Structuring Content With HTML

### Basic HTML Syntax

#### HTML tags

Tags in HTML are not case-sensitive. This means they can be written in uppercase or lowercase. For example, a `<title>` tag could be written as `<title>`, `<TITLE>`, `<Title>`, `<TiTlE>`, etc., and it will work. However, it is best practice to write all tags in lowercase for consistency and readability.

> [!IMPORTANT]
> In order to keep that in mind, write at least a single element in that inconsistent-way\
> Prettier will automatically transfer those inconsistent-tags to lowercased version, that's okay, do it anyway even if it will not be saved

#### Boolean Attributes (HTML)

A `boolean attribute` in HTML is an attribute that represents `true` or `false`
values. If an HTML tag contains a boolean attribute — no matter
the value of that attribute — the attribute is set to `true`
on that element. If an HTML tag does not contain the attribute,
the attribute is set to `false`.

> [!IMPORTANT]
> To keep that the `boolean attribute` concept in your mind, write it at least once,\
> Some examples are: `required`, `readonly`, and `disabled`, you can use one of those if you want.

#### Double Quotes

Both single and double quotes are valid, but for consistency stick to `double quotes` whenever you have to choose between them.\
Wrapping HTML attribute values as an example: `class="first-title"`.

> [!IMPORTANT]
> Use only double quotes in your HTML code whenever needed

### Head Elem: Webpage metadata

The head's job is to contain metadata about the document.

> Dictionary: metadata is information that is given to describe or help you use other information

#### title element

The title element are used in `page tab`\
and also as suggestion name when you try to bookmark a webpage

> [!IMPORTANT]
> Include a `title element` in the `head`.

#### `<meta>` elem

##### meta charset utf-8

`<meta charset="utf-8" />`\
This element specifies the document's character encoding.\
`utf-8` is a universal character set that includes pretty much any character from any human language.

> Some browsers (like Chrome) automatically fix incorrect encodings, so depending on what browser you use, you may not see this problem. You should still set an encoding of `utf-8` on your page anyway to avoid any potential problems in other browsers.

> [!IMPORTANT]
> Include `<meta charset="utf-8" />` in your page.

##### meta with name & content attr

- `name` specifies the type of meta element it is; what type of information it contains.
- `content` specifies the actual meta content.\

Two such meta elements that are useful to include on your page define the author of the page, and provide a concise description of the page.

```html
<meta name="author" content="Chris Mills" />
<meta
  name="description"
  content="The MDN Web Docs Learning Area aims to provide
complete beginners to the Web with all they need to know to get
started with developing websites and applications."
/>
```

> This is good for SEO.

> [!IMPORTANT]
> Include a meta element that include your name\
> And another meta element that include description to the page content\
> Do something similar to the example above

#### favicon

You may see (depending on the browser) favicons displayed in the browser tab containing each open page, and next to bookmarked pages in the bookmarks panel.

A favicon can be added to your page by:

- Saving it in the same directory as the site's index page, saved in .ico format (most also support favicons in more common formats like .gif or .png)
- Adding the following line into your HTML's <head> block to reference it:\
  `<link rel="icon" href="favicon.ico" type="image/x-icon" />`

> [!IMPORTANT]
> Add a favicon to your page,\
> The link element should have `rel`, `href`, and `type` attributes.

#### Applying CSS

Applying CSS done through the `link` element,\
The `link` element should go inside the `head` element, and should have:

- `rel` attribute with value: `stylesheet`,
- `href` attribute with the `css file path` as its value.

Here is how it should be: `<link rel="stylesheet" href="my-css-file.css" />`

> [!IMPORTANT]
> Create an empty css file and link it.
> The `link` elem should have `rel` and `href` attributes with there right values

#### Applying JavaScript

Applying JS Done using the `script` element,\
It should go in the `head` elem, and include the following attributes:

- `src` with `js file path` as it value,
- `defer` which is a `boolean attribute` that basically instructs the browser to load the JavaScript `after` the page has finished parsing the HTML

> [!IMPORTANT]
> Create an empty JS file,\
> The `script` elem should go in the `head`, and should include:
>
> - `src`,
> - and `defer` attributes

#### Setting primary language for the document [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Webpage_metadata#setting_the_primary_language_of_the_document)

This can be done by adding the `lang` attribute to the opening HTML tag as: `<html lang="en-US">`

> Your HTML document will be indexed more effectively by search engines if its language is set (allowing it to appear correctly in language-specific results, for example)\
> and it used by screen readers to use the right language

You can also set subsections of your document to be recognized as different languages.

`<p>Arabic Example <span lang="ar">مرحبا</span></p>`

> [!IMPORTANT]
> Add the `lang` attr to the whole document, use `en` for now,
> and use it for some subsection of the document, maybe for `p`, or `span`

### ✅💻 01 Initial

It is a simple project where I put all the above concepts that is mostly related to metadata that goes in the head elem.

- [code](/projects/html-stage/01-initial/)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/01-initial/index.html)

### Heading & paragraphs in HTML [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Headings_and_paragraphs)

Structured content makes the reading experience easier and more enjoyable.

#### paragraphs

In HTML, each paragraph has to be wrapped in a `<p>` element.

#### headings

There are six heading elements: `h1`, `h2`, `h3`, `h4`, `h5`, and `h6`. Each element represents a different level of content in the document.\

- Preferably, you should use a single `<h1>` per page—this is the top level heading, and all others sit below this in the hierarchy.
- Make sure you use the headings in the correct order in the hierarchy. Don't use `<h3>` elements to represent subheadings, followed by `<h2>` elements to represent sub-subheadings.
- Of the six heading levels available, you should aim to use no more than three per page, unless you feel it is necessary.

> - we need to make sure we are using the correct elements, giving our content the correct meaning, function, or appearance.
> - Semantics has nothing to do with the **LOOK** of the elements, sure the browser by default apply some default styling to elements based on there type, but for example you can style a `p` element to appear like `h1` element using CSS, but that will not change its semantic, it will stay a _paragraph_.

> [!IMPORTANT]
>
> - Always respect the **semantics**.
> - Use a single `h1` element per page.
> - Use at least a single paragraph.
> - Use _no more_ than **three** type of headings unless necessary.
> - Never choose semantic elements for their default style, if you only want to change the _look_ for something use _CSS_.

### ✅💻 02 - Vehicles

This is a fully text-based project, that introduce in a brief manner all the type of vehicles which is _air, road, water vehicles_, and under each type there is some _but not all_ types & vehicles.

- [code](/projects/html-stage/02-vehicles/)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/02-vehicles/index.html)

## Emphasis & Importance [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Emphasis_and_importance)

In HTML we use the `<em>` element to mark up **emphasis**.\
And we use `<strong>` element to mark up **importance**.

> **presentational elements** should no longer be used because, as we've seen before, semantics is so important to accessibility, SEO, etc.\
> For styling you should only use CSS.

> [!WARNING]
> There are [some others](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Emphasis_and_importance#italic_bold_underline%E2%80%A6) that are a bit confusing: `<b>, <i>, and <u>`,\
>  just forget about them now!

> [!IMPORTANT]
> Include `em` and `strong` at least once for each in your page.

## Lists [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Lists)

On the web, we have three types of lists: **unordered**, **ordered**, and **description** lists.

### Unordered lists

Unordered lists are used to mark up lists of items for which the order of the items doesn't matter.\
They are built using the `<ul>` element, which wrap all the list items, each list item should be wrapped in a `<li>` element.

> [!IMPORTANT]
> Include at least a single **unordered list**.

### Ordered lists

Ordered lists are lists in which the order of item _does_ matter.\
The markup structure is the same as for unordered lists, except that you have to wrap the list items in an `<ol>` element, rather than `<ul>`

> [!IMPORTANT]
> Include at least a single **ordered list**.

### Nesting lists

You can create an new list within another list by wrapping new `ol` or `ul` inside a `li` elem.

```html
<ol>
  <li>item 1</li>
  <li>item 2</li>
  <li>
    item 3
    <ul>
      <li>sub-item 1</li>
      <li>sub-item 2</li>
      <li>sub-item 3</li>
    </ul>
  </li>
</ol>
```

> [!IMPORTANT]
> Nest at least one list.
> It doesn't matter if it is nested in `ul` or `ol`.

### Description lists [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Lists#description_lists)

> The purpose of description lists is to mark up a set of items and their associated descriptions, such as terms and definitions, or questions and answers.

It is created by `<dl>`(description list) element,\
Each term is wrapped in a `<dt>` (description term) element,\
And each description definition is wrapped in a `<dd>` (description definition) elem.\

```html
<dl>
  <dt>description term</dt>
  <dd>description definition</dd>

  <dt>description term</dt>
  <dd>description definition</dd>

  <dt>description term</dt>
  <dd>description definition</dd>
</dl>
```

> [!IMPORTANT]
> Include at least a single **description list**.

## Structuring documents

> It's good to understand the overall meaning of all the HTML sectioning elements in detail — this is something you'll work on gradually as you start to get more experience with web development.\
> **So don't try to master them now**

### main [^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)

`<main>` is for content that is unique to the page. Use `<main>` only once per page, and put it directly inside `<body>`.\
Ideally it shouldn't be nested within other elements.

> [!NOTE]
> It could wrap the video you want to watch, or the main story you're reading, or the map you want to view, or the news headlines, etc. This is the one part of the website that definitely will vary from page to page!

> [!IMPORTANT]
> 🎯 Use the `main` element a single time in your pages.\
> 🎯 It should be a _direct_ child to the `body` elem.\
> 🎯 Use it to wrap the _main page content_.

### article [MDN^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article) [WHATWG^](https://html.spec.whatwg.org/multipage/sections.html#the-article-element)

`<article>` encloses a block of related content that makes sense on its own without the rest of the page (e.g., a single blog post).\

The `article` element represents a complete, or self-contained, composition in a document, page, application, or site and that is, in principle, independently distributable or reusable, e.g. in syndication. This could be a **forum post**, a **magazine** or **newspaper article**, a **blog entry**, a **user-submitted comment**, an **interactive widget** or **gadget**, or _any other independent item of content_.\

When **article elements** are **nested**, the _inner article_ elements represent articles that are in principle _related_ to the contents of the outer article. For instance, a blog entry on a site that accepts user-submitted comments could represent the comments as article elements nested within the article element for the blog entry.

> [!IMPORTANT]
> 🎯 Use at least a single `article` element
>
> > At least for the content-based pages.

### section [^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)

`<section>` is similar to `<article>`, but it is more for grouping together a single part of the page that constitutes one single piece of functionality (e.g., a mini map, or a set of article headlines and summaries), or a theme.\
It's considered _best practice_ to _begin_ each section with a **heading**; also note that you can break `<article>`s up into different `<section>`s, or `<section>`s up into different `<article>`s, depending on the context.

> Alway provide an `aria-label` or `arial-labelledby` attributes so that the `section` elem function as you would expect\
> Look at this video in YouTube by [Kevin Powell](https://youtu.be/ULdkpU51hTQ?si=_BKkhZzsRfEFyM_M)

> [!NOTE]
> A **general rule** is that the `section` element is appropriate only if the element's contents would be listed explicitly in the document's **outline**.

> [!IMPORTANT]
> 🎯 The section should have a _heading_\
> Use either `aria-label` or `aria-labelledby` attributes.

#### Other sources

You can use these if you find yourself need more infos:

- [The section element](https://html.spec.whatwg.org/#the-section-element) by WHATWG.

### aside [^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside)

`<aside>` contains content that is not directly related to the main content but can provide additional information indirectly related to it (glossary entries, author biography, related links, etc.).

Some use Cases:

- **Sidebars**: Use `<aside>` for sidebars that contain additional information, links, or advertisements related to the main content.
- **Call-out Boxes**: Use `<aside>` for highlighting important notes or tips that are relevant but not essential to the main text.
- **Author Information**: If you have an article and want to include information about the author, you can use `<aside>`.
- **Related Articles** or Posts: Use `<aside>` to list related articles or posts that readers might find interesting.

> You can look at an article generated by [**MDN AI Help**](https://developer.mozilla.org/en-US/plus/ai-help?c=dd44186f-80a8-468c-88e2-d7df4dbec476)\
> It has some examples and further explanation to the above _use cases_

> [!NOTE]
> Do not use the `<aside>` element to tag parenthesized text, as this kind of text is considered part of the main flow.

> [!IMPORTANT]
> 🎯 Use the `aside` element at least a single time in your pages.\
> You can add:
>
> - an ad that advertise your `Projects Home`,
> - an imaginary ad
> - author biography: _Your biography_
> - an imaginary or real links to some indirectly related articles,
>   - You can use articles from the web, wikipedia as an example.

### header [^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)

`<header>` represents a group of introductory content. If it is a child of `<body>` it defines the global header of a webpage, but if it's a child of an `<article>` or `<section>` it defines a specific header for that section

> [!IMPORTANT]
> 🎯 Include a header element in the page that contains:
>
> - logo
> - page name
> - nav element

> note that as _MDN_ suggests that for accessibility reason it is better to put the `nav` outside of the `header`\
> but to simplify my life for now, I'll put the **nav** inside the **header**

### nav [^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)

The `<nav>` HTML element represents a section of a page whose purpose is to provide **navigation links**, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.

> [!IMPORTANT]
> 🎯 Include the `nav` inside the header,\
> It should include:
>
> - `projects home` button
> - `Universal About` that link to the `main About page`.
>
> If the page contains content, add another `nav section` that contains **table of content**.

### footer [^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer)

`<footer>` represents a group of end content for a page.

> [!IMPORTANT]
> 🎯 Include a `footer` element in your page.\
>
> As a start you can choose from the following:
>
> - **Copyright Information**: Youssef EA 1446 ©.
> - **Navigation Links**: Links to important pages like _projects home_ About Us, Contact, Privacy Policy, Terms of Service.
> - **Contact Information**: add a fake email.
> - **Social Media Links**: add a link to GitHub.

### Non-semantic wrappers [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Structuring_documents#non-semantic_wrappers)

Non-semantic elements should only used if you can't think of a better semantic text element to wrap your content, or don't want to add any specific meaning.\

You have two options:

- `span`: an inline non-semantic element.
- `div` : a block level non-semantic element.

> [!CAUTION]
> use `DIVS` only when there is no better _semantic solution_ and try to **reduce** their usage to the minimum otherwise you'll have a hard time updating and maintaining your documents.

> [!IMPORTANT]
> 🎯 Use the `div` and `span` element only if you need to, with a suitable class.\
> Don't force yourself to use them, since they are well known elements.

### Line breaks & horizontal rules

#### `<br>`: the line break element [^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br)

`<br>` creates a **line break** in a **paragraph**; it is the only way to force a rigid structure in a situation where you want a series of fixed short lines

> It is important because HTML ignore white space and new lines inside paragraphs.

> [!IMPORTANT]
> 🎯 Use at least a single `br` element.

#### `<hr>`: the thematic break element [MDN^](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr) [whatWG^](https://html.spec.whatwg.org/#the-hr-element)

`<hr>` elements create a **horizontal rule** in the document that denotes a **thematic change** in the text (such as a change in topic or scene).\
Visually it just looks like a _horizontal line_.

It used mostly like:

```html
<p>Talking about a specific topic</p>
<!-- hr elem Denote a thematic change-->
<hr />
<p>Change the topic</p>
```

> [!NOTE]
> There is no need for an `hr` element between the sections themselves, since the `section` elements and the `h1` elements imply thematic changes themselves.

> [!IMPORTANT]
> 🎯 Use the `hr` element at least once.

### ✅💻 03 - Qatayef

Qatayef is a web page that will show you step by step how to prepare the well know Lebanese recipe named Qatayef.

- [code](./html-stage/03-qatayef)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/03-qatayef/index.html)

## Advanced text features

> For more details:\
> [MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Advanced_text_features)

### Quotations

#### Blockquote

> For more details:
>
> - [MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Advanced_text_features#blockquotes)
> - [WHATWG](https://html.spec.whatwg.org/multipage/grouping-content.html#the-blockquote-element)

The blockquote element represents a section that is quoted from another source.\

Content inside a **blockquote** must be quoted from **another source**, whose address, if it has one, may be cited in the **cite** attribute.

> [!IMPORTANT]
> 🎯 Use the `<blockquote>` element at least a single time.

#### Inline quotations

Inline quotations work in exactly the same way, except that they use the `<q>` element.\

The **q** element must not be used in place of quotation marks that do not represent quotes

> [!NOTE]
> By **WHATWG:** The use of `q` elements to mark up quotations is entirely _optional_; using **explicit quotation punctuation** without **q** elements is just as correct.

> [!IMPORTANT]
> 🎯 Use at least a single `q` element.

### Abbreviations

The `abbr` element represents an **abbreviation** or **acronym**, optionally with its expansion.\
The `title` attribute may be used to provide an expansion of the abbreviation.\
The _attribute_, if specified, must contain an expansion of the abbreviation, and nothing else.

#### Used for acronym

Here is a basic example:

```html
<p>
  The <abbr>NASA</abbr> word is an acronym, which is an abbreviation consisting
  of the first letters of each word in the name of something, pronounced as a
  word
</p>
```

#### And used for abbreviations

It goes with a **title** attribute, here is a simple example of how to use it:

```html
<p>
  The following are some common abbreviations:
  <abbr title="doctor">Dr</abbr>,<br />
  <abbr title="et cetera">etc</abbr>, <br />
  <abbr title="Digital Versatile Disc">DVD</abbr>,
</p>
```

> [!IMPORTANT]
> 🎯 Use at least a single acronym and wrap it in a `abbr` element.\
> 🎯 Use at least a single abbreviation and give it an expansion with the `title` attr.

### Marking up contact details

It is done using the `<address>` element.

```html
<!-- Example of its use -->
<p>Contact the author of this page:</p>

<address>
  <a href="mailto:youssef@example.com">youssef@example.com</a><br />
  <a href="tel:+14155550132">+1 (415) 555‑0132</a> <br />
  <a href="http://youssef-el-atmani.info">www.youssef-el-atmani.info</a>

  Hay Erraha, <br />
  Berrechid. <br />
  26100 <br />
</address>
```

it can include various types of contact information, such as:

- Email Addresses: Typically represented using the `mailto:` link.
- Phone Numbers: Usually represented using the `tel:` link.
- Physical Addresses: This can include street addresses, city, state, and postal codes.
- Web Addresses (URLs): Links to websites or social media profiles.

> [!NOTE]
> It is typically used within the context of an `<article>` or `<footer>` element.

> [!IMPORTANT]
> 🎯 Use the `address` element in your footer for your contact data
>
> - GitHub
> - Email
>
> 🎯 If you have some article based content such as blog, add an address for it that contain the contact info for the writer.

### Superscript and subscript

They are useful when writing special mathematical formulas, or chemical formulas:\

- Rand equation: x<sup>3</sup> + 3x<sup>2</sup> + 7x + 8 = 0 **sup element**
- Sugar Formula: C<sub>12</sub>H<sub>22</sub>0<sub>11</sub> **sub element**

> [!IMPORTANT]
> 🎯 Use at least a single **sup**.\
> 🎯 Use at least a single **sub** element

### Representing computer code [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Advanced_text_features#representing_computer_code)

`<code>`: For marking up generic pieces of computer code.\
`<pre>`: For retaining whitespace (generally code blocks).\
`<var>`: For specifically marking up variable names.\
`<kbd>`: For marking up keyboard (and other types of) input entered into the computer.\
`<samp>`: For marking up the output of a computer program.

> [!IMPORTANT]
> 🎯 Either find a place for them in your page, or in case it was _meaningless_, add a simple page where you use all those elements `code, pre, ...`, and link it in the footer element in your home page of the new created projects.

### Marking up times and dates

HTML provides the `<time>` element for marking up times and dates in a machine-readable format.

As an example:

```HTML
<time datetime="2025-04-05"> 05 / 04 / 2025</time>
```

The time element represents its contents, along with a machine-readable form of those contents in the datetime attribute. The kind of content is limited to various kinds of dates, times, time-zone offsets, and durations.\

The datetime attribute may be present. If present, its value must be a representation of the element's contents in a machine-readable format.\

The datetime value of a time element is the value of the element's datetime content attribute, if it has one, otherwise the child text content of the time element.\

> [!NOTE]
> A time element that does not have a datetime content attribute must not have any element descendants.

> [!IMPORTANT]
> 🎯 Use the `time` element at least once.\
> Possible use cases:
>
> - Use it in the footer for the time of completing each project.

## Creating links [M^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links)

Links (also known as hyperlinks) are really important — they are what makes the Web a web.

> [!NOTE]
> A **URL** can point to HTML files, text files, images, text documents, video and audio files, or anything else that lives on the Web.

### Block level links

> You can wrap anything within an anchor element, even block element such as heading elements or paragraphs, even whole sections.\
> As long as there is no interactive content within (e.g., buttons or other links).

For example you can convert an `h1` element into a _link_ by wrapping it by an `anchor` element.

> [!IMPORTANT]
> 🎯 Convert _block level_ elements such as header elements or sections if needed, as long as they do not contain interactive elements.

### title attribute

The title contains additional information about the link, such as which kind of information the page contains, or things to be aware of on the website.

> [!NOTE]
> The **title** information is only accessible when hovered by the mouse cursor, which mean it will be hard to get that when using a keyboard or a touching screen.\
> So if that title information is something really important to all users, you should for example include that information in a _regular text_ rather than using the **title** attribute.

> [!IMPORTANT]
> 🎯 I think that the _title element_ should be avoided, but just use it once to stay aware of it.

### Document fragments

> Dictionary: A fragment is a small piece or a part, especially when broken from something whole.

You can also link to a **document fragment** using the `anchor` element alongside with the `id` attribute.\

This is how you can navigate between different section within the same page, or link to specific section rather than the whole page; _rather than the start of the page_.

```html
<!-- Some place at the top of the page-->
<p>
  The <a href="#Mailing_address">company mailing address</a> can be found at the
  bottom of this page.
</p>

<!-- The bottom of the page -->
<h2 id="Mailing_address">Mailing address</h2>
<p>The mailing address section</p>
```

> [!IMPORTANT]
> 🎯 If you have a text content based project, create a _table of content_ that links to different sections of your project

### Absolute VS Relative URLs

#### Absolute URL

It points to a location defined by its absolute location on the _web_, including **protocol** and **domain name**.\
An **absolute URL** will always point to the same location, no matter where it's used.

#### Relative URL

It points to a location that is relative to the file you are linking from.

### Link best practices [M^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links#link_best_practices)

- Use clear link wording, it is helpful for:

  - Search Engines,
  - Accessibility,
  - Descriptive link is useful for _visual readers_.
    - ✅ **Good link _text_:** [Download Firefox](https://www.mozilla.org/en-US/firefox/).
    - 🚫 **Bad link _text_:** [Click here](https://www.mozilla.org/en-US/firefox/) to download firefox.

- Don't repeat the URL as part of the link text.
  - URLs looks ugly,
  - and even sounds uglier when screen readers read them letter by letter.
- Don't say "link" or "link to" in the _link text_
  - Screen readers tell people there's a link.
  - Visual readers rely on the well known styling of a link
    - styled in a different color and underlined. (this convention generally shouldn't be broken, as users are used to it).
- Keep your link text as short as possible
  - this is helpful because screen readers need to interpret the entire link text.
    - a _shorter_ link text is easier to understand.
- When linking to non-HTML resources — You should leave a clear signposts
  - you should add clear wording to the link text about what is going to happen.
    - ex1: [Watch the video (stream opens in separate tab, HD quality)]()
    - ex2: [Download the sales report (PDF, 10MB)]()

#### Download attribute

When you are linking to a resource that's to be downloaded rather than opened in the browser, you can use the download attribute to provide a default save filename.

```html
<a
  href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=en-US"
  download="firefox-latest-64bit-installer.exe"
>
  Download Latest Firefox for Windows (64-bit) (English, US)
</a>
```

> [!IMPORTANT]
> 🎯 For links, keep the different color, and the underlying line. you can either use the default style, or make your own, but always keep that, since the users are used to that: _Links are underlined and have different color_.\
> 🎯 Keep the link text as short and clear as possible.\
> 🎯 Do not use the `same link text` to link to different places within the same page.\
> 🎯 Style the link with a different color and an underlined it, or keep the default styling, unless your link is living in a place where it is obvious that it is a link.\
> 🎯 When linking to non-HTML resources — You should leave a clear signposts

#### When to open links into a new tab [M^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links#when_to_open_links_in_a_new_tab)

> [!NOTE]
> If you do open links in new tabs, then it is recommended that you provide cues for these links, such as an icon next to the link text [empty link↗]().

> [!IMPORTANT]
> 🎯 Open internal links in the **same tab**,\
> 🎯 and external links in **new tabs**, with the following icon **↗**,

### ✅💻 04 - BYDH

BYDH-**Build Your Dream Home**, is a website that will walk you through all the steps that you should take when you want to build a house.

- [code](./html-stage/04-BYDH/)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/04-BYDH/index.html)

## HTML images

### file image name

Search engines also read image filenames and count them towards SEO.\
Therefore, you should give your image a descriptive filename; _dinosaur.jpg_ is **better** than _img835.png_.

> [!IMPORTANT]
> 🎯 Give images a descriptive name

> [!WARNING]
> Never point the `src` attribute at an image hosted on someone else's website without permission. This is called "hotlinking".

> [!NOTE]
> Elements like `<img>` and `<video>` are sometimes referred to as replaced elements. This is because the element's content and size are defined by an external resource (like an image or video file)

### Alternative Text

Its value is supposed to be a textual description of the image, for use in situations where the image cannot be seen/displayed or takes a long time to render because of a slow internet connection.

> [!NOTE]
> If you are using HTML img for decoration, use an empty `alt`: **alt=""**,\
> Decorative images are preferred to be added as `background-image` using CSS.

### width and height

Use them so that the content do not jump once the image get downloaded and displayed.\
Knowing how to use them with responsive displays is an **advanced** topic, only use them for whatever monitor your using.

> [!IMPORTANT]
> 🎯 Use the **width** and **height** with `img` element

### Caption

To add a caption to an image use the `figure` element along with the `figcaption`.

> [!NOTE]
> From an **accessibility** viewpoint, captions and alt text have distinct roles. `Captions` benefit even people who can see the image, whereas `alt` text provides the same functionality as an absent image.\
> Therefore, `captions` and `alt text` shouldn't just say the same thing, because they both appear when the image is gone. Try turning images off in your browser and see how it looks.

> [!IMPORTANT]
> 🎯 Use the **caption** at least once for an image

### CSS background-image

if an image has meaning, in terms of your content, you should use an HTML image. If an image is purely decoration, you should use CSS background images.

> [!IMPORTANT]
> 🎯 Include meaningful images using `html images`.
> 🎯 Include decorative images with `CSS` as **background-images**.

### ✅💻 05 - Bird Species

A simple website about birds, sharing popular species, fun facts.

- [code](./html-stage/05-generic/plus/index.html)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/05-generic/plus/index.html)

## HTML video

[HTML Video--MDN lesson](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio#the_audio_element)

The `<video>` element allows you to embed a video.
you can either include the video path in a `src` attr as follow in the open video tag:

```html
<video src="path.mp4"></video>
```

or include the path, in a separate `source` element, which is a void element, as follow:

```html
<video>
  <source src="path.mp4" type="video/mp4" />
  <source src="path.webM" type="video/webm" />
</video>
```

> [!NOTE]
> Adding a `type` attribute is _optional_, but it is **important**, because when it is defined, the browser will skip the formats that doen't support,\
> but if is not defined, then the browser will render the video, and then check if it can play it, if it can't, then it will move to the next available source if there is any, which consume time, and bandwidth.

### attributes

- `src=""`: for the video path.
- `controls`: Give the users the ability to control the video.
- `loop`: is a **boolean attr** make the video play again and again: _❗Should be avoided❗_
- `muted`: is a **boolean attr** Causes the media to play with the sound turned off by default.
- `poster=""`: The URL of an image which will be displayed before the video is played.
- `preload=""`: Used for buffering large files; it can take one of three values: `none, auto, metadata`.
- `width`:
- `height`:

### Fallback content

It will be displayed if the browser accessing the page doesn't support the `<video>` element, allowing us to provide a fallback for older browsers.

```html
<video src="rabbit320.webm" controls>
  <p>
    Your browser doesn't support HTML video. Here is a
    <a href="rabbit320.webm">link to the video</a> instead.
  </p>
</video>
```

> [!IMPORTANT]
> 🎯 Use the **video** element, with the following attributes:
>
> - src, controls, muted, width, height, poster.
>
> Include the `src` in the `source` element.\
> Include a **fallback** paragraph.

## HTML audio

It is similar to the `HTML video` element, with one difference:

- it does not support: `width/height`,
- it does not support: `poster`.

> [!IMPORTANT]
> 🎯 Use the `audio` element, with the typical attributes.

## Displaying video text tracks [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio#displaying_video_text_tracks)

```html
<!-- Track Code Example-->
<video controls>
  <source src="example.mp4" type="video/mp4" />
  <source src="example.webm" type="video/webm" />
  <track
    kind="subtitles"
    src="subtitles_ar.vtt"
    srclang="ar"
    label="Arabic"
    default
  />
</video>
```

To display text tracks in a video, we use the `<track>` element, which is a void element, it accept multiple attributes.\
Here is a list of the attributes it accept:

- **default**: This attribute indicates that the track should be enabled unless the user's preferences indicate that another track is more appropriate. This may only be used on one track element per media element.
- **kind**: How the text track is meant to be used.\
  If omitted the _default_ kind is `subtitles`.\
  If the attribute contains an invalid value, it will use `metadata`.\
  The following keywords are allowed:
  - _subtitles_
  - _captions_
  - _metadata_: Tracks used by scripts. Not visible to the user.
- **label**: A user-readable title of the text track which is used by the browser when listing available text tracks.
- **src**: Address of the track file (`.vtt` file).
- **srclang**: Language of the track text data. It must be a valid BCP 47 language tag.\

> [!NOTE]
>
> - If the **kind** attribute is set to `subtitles`, then **srclang** _must be defined_.
> - The default value of the **kind** attribute is `subtitles`.
> - The `<track>` elem should be placed within `<audio>` or `<video>`, but **after all** `<source>` elements.

> For more details, including on how to add labels, read [Adding captions and subtitles to HTML video](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video) by MDN.

### ✅💻 06 - Audio & Video

A simple webpage to practice what I've learned until now

- [code](./html-stage/06-audio-video/)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/06-audio-video/index.html)

## HTML table basics

### Structure

- `<table>`: Encapsulates the entire table.
- `<tr>`: Defines a table row.
- `<td>`: Defines a standard data cell within a row.
- `<th>`: Defines a header cell, typically used to label columns or rows.​

### Creating a Basic Table

1. Start with the `<table>` tag to create the table structure.
2. Use `<tr>` to define a row within the table.
3. Within each `<tr>`, use `<td>` for data cells or `<th>` for header cells.

```html
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
  </tr>
</table>
```

### Spanning Rows and Columns

- `colspan`: Allows a cell to span multiple columns.
- `rowspan`: Allows a cell to span multiple rows

## HTML table accessibility

Accessible tables are crucial for users relying on assistive technologies. Proper structuring and semantic markup ensure that screen readers and other tools can interpret and navigate tables effectively.

### Adding Captions

It is done by the `<caption>` element.

- **Purpose**: Provides a concise description of the table's content.

- **Placement**: Must be **the first child** of the `<table>` element.

- **Benefit**: Enhances understanding for all users, especially those using screen readers.​

### Structuring the table

It is done using `<thead>`, `<tbody>`, and `<tfoot>` elements.\

- These tags define table sections:
  - `<thead>` for header rows.
  - `<tbody>` for the main content.
  - `<tfoot>` for summary rows.
- Improves organization and clarity in the code structure.
- Makes the table easier to style using CSS.
  - Which makes the table easier to read and maintain.

### Using scope with `<th>`

- Defines how a header cell relates to data cells.
- Values:
  - **col** for column headers.
  - **row** for row headers.
  - **colgroup** and **rowgroup** for grouped headers.
- Helps assistive technologies identify the correct header for each cell.

```html
<!-- Code example -->
<thead>
  <tr>
    <th scope="col">Purchase</th>
    <th scope="col">Location</th>
  </tr>
  <tr>
    <th scope="row">Date</th>
    <td>table cell</td>
  </tr>
</thead>
```

### id and headers for complex tables

> [!NOTE]
> Use this method only when `scope` isn’t enough (e.g., multiple header levels).

To use it, you should:

- Assign **id** attributes to header cells (`<th>`).
- Reference those **ids** in the **headers** _attribute_ on data cells (`<td>`).

```html
<!-- Code Sample -->
<thead>
  <tr>
    <th id="clothes" colspan="3">Clothes</th>
  </tr>
  <tr>
    <th id="trousers" headers="clothes">Trousers</th>
    <th id="skirts" headers="clothes">Skirts</th>
    <th id="dresses" headers="clothes">Dresses</th>
  </tr>
</thead>
<tbody>
  <tr>
    <th id="belgium" rowspan="3">Belgium</th>
    <th id="antwerp" headers="belgium">Antwerp</th>
    <td headers="antwerp belgium clothes trousers">56</td>
    <td headers="antwerp belgium clothes skirts">22</td>
    <td headers="antwerp belgium clothes dresses">43</td>
  </tr>
</tbody>
```

### Assignment 📌

- **Assignment Goal 🎯**: To practice _table structure_ and _table accessability_.

> [!NOTE]
> The following table is taken from **mdn learning-area**, You can find the original code at
> [items-sold.html](https://github.com/mdn/learning-area/blob/main/html/tables/advanced/items-sold.html)\
> I have slightly changed it so that I can write some elements by my hands.

Take the following table as a starting point:

```html
<table>
  <tr>
    <td></td>
    <th>Clothes</th>
    <th>Accessories</th>
  </tr>
  <tr>
    <th>Trousers</th>
    <th>Skirts</th>
    <th>Dresses</th>
    <th>Bracelets</th>
    <th>Rings</th>
  </tr>

  <tr>
    <th>Belgium</th>
    <th>Antwerp</th>
    <td>56</td>
    <td>22</td>
    <td>43</td>
    <td>72</td>
    <td>23</td>
  </tr>
  <tr>
    <th>Gent</th>
    <td>46</td>
    <td>18</td>
    <td>50</td>
    <td>61</td>
    <td>15</td>
  </tr>
  <tr>
    <th>Brussels</th>
    <td>51</td>
    <td>27</td>
    <td>38</td>
    <td>69</td>
    <td>28</td>
  </tr>
  <tr>
    <th>The Netherlands</th>
    <th>Amsterdam</th>
    <td>89</td>
    <td>34</td>
    <td>69</td>
    <td>85</td>
    <td>38</td>
  </tr>
  <tr>
    <th>Utrecht</th>
    <td>80</td>
    <td>12</td>
    <td>43</td>
    <td>36</td>
    <td>19</td>
  </tr>
</table>
```

#### Instructions

- Make the headers span their relative columns and rows
  - The table should look like [items-sold-headers.html<sup>by MDN</sup>](https://mdn.github.io/learning-area/html/tables/advanced/items-sold-headers.html).
- Add the following **caption** to the `table`: _Items Sold August 2016_
  - Recall that the caption should be the first child of the `table`
- Differentiate the `table header` and `table body`
- Write a **footer** for the table, and make sure it is recognized by the browser as a `table footer`.
- Duplicate the table.
- Now you have two identical tables.
  - Improve the accessability of the first table using the _basic method_.
  - For the other table, use the _advanced & explicit method_.

#### Additional Assignment

follow the steps along the [Challenge: Structuring a planet data table <sup>MDN</sup>](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Planet_data_table)

> [!NOTE]
> Use the bellow markdown, not the one provided by MDN, since the planet names provided have _polytheism relation_\
> In the bellow markdown I only changed the `polytheism words`, and everything else is identical to the original text provided by MDN.

```
Rows

Terrestrial planets

Utared 0.330 4,879 5427 3.7 4222.6 57.9 167 0 Closest to the Sun
Zuhara 4.87 12,104 5243 8.9 2802.0 108.2 464 0
Ard 5.97 12,756 5514 9.8 24.0 149.6 15 1 Our world
Mirrikh 0.642 6,792 3933 3.7 24.7 227.9 -65 2 The red planet

Gas and Ice Giants

Gas giants

Mushtari 1898 142,984 1326 23.1 9.9 778.6 -110 67 The largest planet
Zuhal 568 120,536 687 9.0 10.7 1433.5 -140 62

Ice giants

Sabi'a 86.8 51,118 1271 8.7 17.2 2872.5 -195 27
Thamina 102 49,528 1638 11.0 16.1 4495.1 -200 14

Dwarf planets\*

Tasi'a 0.0146 2,370 2095 0.7 153.3 5906.4 -225 5 Declassified as a planet in 2006, but this <a href="http://www.usatoday.com/story/tech/2014/10/02/pluto-planet-solar-system/16578959/">remains controversial</a>.

Columns

Name
Mass (10<sup>24</sup>kg)
Diameter (km)
Density (kg/m<sup>3</sup>)
Gravity (m/s<sup>2</sup>)
Length of day (hours)
Distance from Sun (10<sup>6</sup>km)
Mean temperature (°C)
Number of moons
Notes

Caption

Data about the planets of our solar system (Planetary facts taken from <a href="http://nssdc.gsfc.nasa.gov/planetary/factsheet/">Nasa's Planetary Fact Sheet - Metric</a>).
```

### ✅💻 07 - HTML Tables

A simple webpage to practice everything I've learned until now.

- [code](./html-stage/07-html-tables)
- [live preview](https://youssef-el-atmani.github.io/MDN-Based-Projects/projects/html-stage/07-html-tables/index.html)

## HTML Forms

**Buttons** are usually created using HTML `<button>` elements (they are also sometimes created using `<input>` elements with their type attributes set to a value like **button** or **submit**).\
\
**Forms** are created using elements such as `<form>`, `<label>`, `<input>`, and `<select>`.

### The anatomy of a form

- A `<form>` element, which wraps all of the other form content.\
- One or more pairs each consisting of a `<label>` element and a `form control` element (usually an `<input>` element, but there are other types as well, for example `<select>`)\
- A `<button>` element, used to submit the form.

#### The `<form>` element

```html
<form action="./submit_page" method="get"></form>
```

The `<form>` element acts as the outer wrapper for the form, grouping together all the form controls inside it. When the `<button>` is pressed, all the data represented by the **form controls** will be _submitted_ to the server. The `<form>` element can take many attributes, but the two most important ones, are as follows:

- **action**: Contains a path to the page that we want to send the submitted form data to, to be processed.
- **method**: Specifies the data transmission method you want to use for sending the form data to the server.

#### Structuring forms

##### Including HTML elements

You can include any HTML elements you like inside a `<form>` element to structure the form elements themselves and provide containers to target with CSS for styling, etc, _look to the following code snippet_:

```html
<form action="./submit_page" method="get">
  <h2>Subscribe to our newsletter</h2>
</form>
```

##### Separating form elements

Some people use `<p>` elements to separate out their **form elements**, some use `<div>`, `<section>`, or even `<li>` elements. It doesn't matter a great deal, _as long as the elements used make semantic sense_.

##### Grouping form elements

**fieldset** elem is used to group a set of related **form element**, such as multiple _checkboxes_ and _radio_ buttons.

#### input element

The `<input>` elements represent the different data items entered into the form.\
\
Take the following example:

```html
<input type="text" name="name" id="name" required />
```

The attributes are as follows:

- **type**: Specifies the *type*of form control to create. There are many different types of form controls, from **simple text** fields of different types to **radio buttons**, **checkboxes**, and more.
- **name**: Specifies a name for the data item. When the form is submitted, the data is sent in **name/value** pairs.
- **id**: Specifies an ID that can be used to identify the element. In this case, it is used to associate the form control with its `<label>`.
- **required**: Specifies that a value has to be entered into the form element before the form can be submitted.

> [!NOTE]
> Some input types usually don't get their values from text entered into a field. For example, `<input type="color">` renders a color picker widget that you choose a color from.

> [!NOTE]
> For radio buttons you should provide a **value** attribute, where you specify the value that will be submitted if a specific button has been checked.\
> Note that you can specify a `value` attribute on input types like **text** and **color** — the effect is that the value is pre-filled into the form field when it is first rendered

##### Some form control types:

- text
- number
- email
- password
- color
- tel
- radio
- checkbox

#### the label elem [^](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_forms#label_elements)

`<label>` elements provide identifying labels associated with form controls that describe the data that should be entered into them.

```html
<!-- Usage of label elem  -->
<label for="name">Name (required):</label>
<input type="text" name="name" id="name" required />
```

`<label>` elements are important for several reasons, most notably that:

- For visually impaired users.
- They enable you to focus the form elements by clicking on their label text as well as the controls.

##### Explicit and implicit form labels

You can implement an implicit form label by nesting the control inside the label, like this:

```html
<!-- implicit form label -->
<!-- MDN: Not Preferred, Use the Explicit instead! -->
<label>
  Name (required):
  <input type="text" name="name" required />
</label>
```

The nesting makes an implicit association between control and label, and you no longer need the **id** and **for** attributes.

> [!NOTE]
> According to MDN, the **explicit** label approach is preferred.

#### The button elem

When a `<button>` element is included inside a `<form>` element, its default behavior is that it will submit the form.\
\
There are other button behaviors that can be specified via the `<button>` element's type attribute:

- `<button type="submit">` **explicitly** declares that a button should behave like a **submit button**.
  - You don't ever really need to declare this, unless for some reason you are including other buttons inside your `<form>`.
- `<button type="reset">` creates a reset button — this immediately deletes all data out of the form, resetting it to its initial state.
  - 🚫⚠️ **Don't ever use reset buttons** .. Most people have experienced filling out a long form only to click the reset button by accident
- `<button type="button">` creates a button with the same behavior as buttons specified outside of `<form>` elements.

> [!NOTE]
> You can also create the above button types using an `<input>` element with the same type values specified — `<input type="submit">`, `<input type="reset">`, and `<input type="button">`. However, these have **many disadvantages** compared to their `<button>` counterparts. You should use `<button>` instead.

### Other control types

#### Radio buttons

```html
<form>
  <!-- Male or Female -->
  <fieldset>
    <legend>What is your gender? (Required)</legend>
    <input type="radio" name="gender" value="Male" id="male-gender" checked />
    <label for="male-gender">Male</label>

    <input type="radio" name="gender" value="Female" id="female-gender" />
    <label for="female-gender">Female</label>
  </fieldset>
</form>
```

radio buttons are implemented using `<input type="radio">` controls.\
These render as a set of push button controls where only one of the set can be selected at any one time.\
\
**radio** input types mostly work the same as text input types, but with a few differences

- The name attributes for each set of radio buttons have to contain the same value, to associate them together as one set.
- You have to include a value attribute containing the value to submit for each radio button.
- The `<label>` for each radio button should describe that particular value choice, rather than the overall value you are selecting.

> [!NOTE]
> The preferred way to provide a description of the overall value choice is to wrap them in a `<fieldset>`, which takes a `<legend>` element as a child that contains the description.

### Disabling form controls

It is done using `disabled` boolean attribute, you can either disable a **single** form element, or an entire set of form element that fall within the the `fieldset` boundaries, you can also **disable** a button element.

#### Checkboxes

It is implemented using `<input type="checkbox"> `.
\
\
radio buttons and checkboxes are implemented in a very similar way (they can also take **checked** attributes to render them pre-selected when the page loads). They also behave in a fairly similar fashion, except that **radio buttons** allow you to choose zero or one items out of many, and **checkboxes** allow you to choose zero or more items out of many.

---

```html
<input type="checkbox" id="white-color" name="white" />
<label for="white-color">White</label>

<input type="checkbox" id="blue-color" name="blue" />
<label for="blue-color">Blue</label>
```

The main difference (`apart from the type value!`) is that each **checkbox**
has a **different name value**, and they generally **aren't given value
attributes**. Behavior-wise, this means they represent different data values,
whereas a radio button set only represents one. On submission, each value is
submitted with a value of on if the checkbox was checked — `blue=on`, `white=on`, etc.

---

#### Drop-down menus

Implemented using the **selection control**.

```html
<label for="transport">How are you getting here:</label>
<select name="transport" id="transport">
  <option value="">--Please choose an option--</option>
  <option value="plane">Plane</option>
  <option value="bike">Bike</option>
  <option value="walk">Walk</option>
  <option value="bus">Bus</option>
  <option value="train">Train</option>
  <option value="jetPack">Jet pack</option>
</select>
```

If you _don't_ specify a **value** inside the **option**, the **text** inside the `<option></option>` tags is used as the **value**.

> [!NOTE]
> If you want to have a specific option selected on page load, you can add a **selected** attribute to the relevant `<option>` element.

#### Multi-line text input fields

Multi-line text input fields are created using `<textarea>` elements:

```html
<label for="comments">Any other comments:</label>
<textarea id="comments" name="comments" rows="5" cols="33"></textarea>
```

They behave in the same way as `<input type="text">` elements, **except** that they allow multiple lines of text to be entered. The rows attribute specifies the number of rows tall the text area will be by default, while the cols attribute specifies the number of columns wide the text area will be by default.\
If they are not specified, the values used are _cols="20" and rows="2"_.

### Form Assignment

**The Goal**: to be comfortable with creating HTML forms, and to remember all it different parts.

---

- create a form element
- add a path where the data will be sent
- add a method

---

Add the following title to the form: **Practice Writing Forms**

---

- Take the **user name**, it should be required.
- Take the **user age**.
- Take the **user gender**, required.
- Take the **user email**.
- Take the **user phone**.
- Ask the user : **What you've learned**, and give him the following options:
  - HTML
  - CSS
  - JS
  - React
- Ask the user for his goal: **What is your Goal?**
  - --Choose One--
  - Front End
  - Back End
  - Full Stack
- Give the user the ability to **Leave a message**
- Add a **submit** button
- Add a **reset** button, test it, and remove it, since it should be avoided
