---
theme: apple-basic

# https://sli.dev/custom/highlighters.html
highlighter: shiki

# show line numbers in code blocks
# lineNumbers: true

# some information about the slides, markdown enabled
info: |
  ## HTML walkthrough
  A presentation about news and tricks

# favicon, can be a local file path or URL
favicon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/2560px-HTML5_logo_and_wordmark.svg.png'

# fonts will be auto imported from Google fonts
# Learn more: https://sli.dev/custom/fonts


layout: intro
image: 'https://images.unsplash.com/photo-1542202229-7d93c33f5d07?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2670&q=80'
---



  # HTML
  ## (or How To Make Lasagna)



<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---
layout: section
---

# Table of content


  1. Content sectioning Do's & Dont's
  2. Common a-tag mistakes
  3. `<img>` news


---
layout: bullets
---

# Part 1 - Content sectioning



  - `<header>`
  - `<nav>`
  - `<main>`
  - `<section>`
  - `<article>`
  - `<footer>`

---
layout: default
---

#  [`<header>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)

<div grid="~ cols-2 gap-8" class="">
<div>


Introductory content, typically a group of introductory or navigational aids. It may contain some heading elements but also a logo, a search form, an author name, and other elements.


## Takeaways 

* Not a sectioning content and therefore does not introduce a new section 
* `<header>` element is intended to usually contain the surrounding section's heading (an h1–h6 element), but this is not required. 

</div>
<div class="flex flex-col gap-8">



```html 
<header>
  <h1>Main Page Title</h1>
  <img src="logo.png" alt="Acme Inc logo">
</header>
```

</div>
</div>




---
layout: default
---

#  [`<nav>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)

<div grid="~ cols-2 gap-8" class="">
<div>

The `<nav>` HTML element represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.


</div>
<div class="flex flex-col gap-8">


```html 
<nav class="crumbs">
    <ul>
        <li><a href="/bikes">Bikes</a></li>
        <li><a href="/bmx">BMX</a></li>
        <li><a href="/jump-bike">Jump Bike 3000</a></li>
    </ul>
</nav>
```

</div>
</div>

## Takeaways
* It's not necessary for all links to be contained in a `<nav>` element. `<nav>` is intended only for major block of navigation links; typically the `<footer>` element often has a list of links that don't need to be in a `<nav>` element.
* A document may have several `<nav>` elements, for example, one for site navigation and one for intra-page navigation. aria-labelledby can be used in such case to promote accessibility, see example.



<div class="abs-br px-4">
<a href="https://html.spec.whatwg.org/multipage/sections.html#the-nav-element">
WHATWG
</a>
</div> 





---
layout: default
---

#  [`<main>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)

<div grid="~ cols-2 gap-8" class="">
<div>


Represents the dominant content of the `<body>` of a document. The main content area consists of content that is directly related to or expands upon the central topic of a document, or the central functionality of an application.

## Takeaways 

* The content of a `<main>` element should be unique to the document 
* Content that is repeated across a set of documents or document sections such as sidebars, navigation links, copyright information, site logos, and search forms shouldn't be included unless the search form is the main function of the page.
 Påverkar inte DOM-strukturen, utan endast informativ (T.ex. för screen-readers) 
- Användbart vid “skipnav” funktion (exempel här https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main) (bättre exempel - https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#skip_links) 

</div>
<div class="flex flex-col gap-8">



```html 
<body>
  <a href="#content" class="skip-link">
    Skip to main content
  </a>
  <header>
    …
  </header>
  <main id="content"> 
    <!-- The skip link jumps to here -->
  </main> 
</body>
```

</div>
</div>

<div class="abs-br px-4">
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main">
MDN
</a>
</div> 


---
layout: default
---

#  [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)

<div grid="~ cols-2 gap-8" class="">
<div>

Represents a generic standalone section of a document, which doesn't have a more specific semantic element to represent it. 
## Takeaways 

*  `<section>` should only be used if there isn't a more specific element to represent it
*  Sections **should always have a heading** (`<h1>`-`<h6>` element), with very few exceptions.
* If the contents represent useful tangential information that works alongside the main content, but is not directly part of it (like related links, or an author bio), use an `<aside>`.
*	If you are only using the element as a styling wrapper, use a `<div>`. A rule of thumb is that a `<section>` should logically appear in the outline of a document.

</div>
<div class="flex flex-col gap-8">



```html 
<!-- Does your code look like this? -->
<div>
  <h2>Heading</h2>
  <p>Bunch of awesome content</p>
</div>

<!-- That's a perfect place for <section> -->
<section>
  <h2>Heading</h2>
  <p>Bunch of awesome content</p>
</section>
```

</div>
</div>

<div class="abs-br px-4">
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main">
MDN
</a>
</div> 


---
layout: default
---

#  [`<article>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article)

<div grid="~ cols-2 gap-8" class="">
<div>

A forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.
## Takeaways 
*	Each `<article>` should be identified, typically by including a heading  (`<h1>`-`<h6>` element) as a child of the `<article>` element.
*	When an `<article>` element is nested, the inner element represents an article related to the outer element. For example, the comments of a blog post can be `<article>` elements nested in the `<article>` representing the blog post.

</div>
<div class="flex flex-col gap-8">



```html 
<article class="forecast">
    <h1>Weather forecast for Seattle</h1>
    <article class="day-forecast">
        <h2>03 March 2018</h2>
        <p>Rain.</p>
    </article>
    <article class="day-forecast">
        <h2>04 March 2018</h2>
        <p>Periods of rain.</p>
    </article>
    <article class="day-forecast">
        <h2>05 March 2018</h2>
        <p>Heavy rain.</p>
    </article>
</article>

```

</div>
</div>

<div class="abs-br px-4">
<a href="https://html.spec.whatwg.org/multipage/sections.html#the-article-element">
WHATWG
</a>
</div> 

---
layout: default
---

#  [`<footer>`](https://html.spec.whatwg.org/multipage/sections.html#the-footer-element)

<div grid="~ cols-2 gap-8" class="">
<div>


represents a footer for its nearest sectioning content or sectioning root element.

## Takeaways 

* Enclose information about the author in an `<address>` element that can be included into the `<footer>` element.
* The `<footer> `element is not sectioning content and therefore doesn't introduce a new section in the outline.

</div>
<div class="flex flex-col gap-8">



```html 
<article>
    <h1>How to be a wizard</h1>
    <ol>
        <li>Grow a long, majestic beard.</li>
        <li>Wear a tall, pointed hat.</li>
        <li>Have I mentioned the beard?</li>
    </ol>
    <footer>
        <p>© 2018 Gandalf</p>
    </footer>
</article>

```

</div>
</div>

<div class="abs-br px-4">
<a href="https://html.spec.whatwg.org/multipage/sections.html#the-footer-element">
WHATWG
</a>
</div> 


---
layout: bullets
---
# Part 2 - Common a-tag mistakes

  - Confused with onclick-event
  - Bad indication where the link goes
  - Size / margin




---
layout: default
---

#  [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) - common mistakes


Combined with onclick-event - use `<button>` instead

```html {all|3}
<div class="wrapper">
    <a class="js-menu-handler" 
      href="javascript:;">
      <img src="/svg/hamburger.svg">
    </a>
</div>
```


---
layout: default
---

# [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) - common mistakes

The content inside a link should indicate where the link goes, even out of context.
```html {all|3|8}
<!-- Inaccessible, weak link text -->
<p>
  Learn more about our products <a href="/products">here</a>.
</p>

<!-- Strong link text -->
<p>
  Learn more <a href="/products">about our products</a>.
</p>
```



---
layout: default
---

# [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) - common mistakes


* Size - A minimum size of `44×44` CSS pixels is recommended.
* room between links - https://axesslab.com/hand-tremors/

 ![Touch targets](/assets/Touchtargets.png.webp)

---
layout: iframe

# the web page source
url: https://www.youtube.com/embed/BE5WRtWPmAw
---

---
layout: fact
---
# `<img>` 
news
  

---
layout: image-right
image: '/assets/loading-lazy.png'
---
#  [`<img>`](https://html.spec.whatwg.org/multipage/images.html)


* [`loading="lazy"`](https://caniuse.com/loading-lazy-attr) has full browser support since March 14th 2022



<div class="abs-br px-4">
<a href="https://html.spec.whatwg.org/multipage/images.html">
WHATWG
</a>
</div> 


---
layout: center
class: text-center
---

# Learn More

[whatwg docs](https://html.spec.whatwg.org/multipage/) · 
[mdm docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) · [link to slides](https://html-presentation-carljohan.vercel.app/)
