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
