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
  ## (How To Make Lasagna)



<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: default
---

# `<a>` : [The Anchor element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)

<div grid="~ cols-2 gap-4">
<div>

The anchor element, with its href attribute, creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address.

Content within each `<a>` should indicate the link's destination.


</div>
<div class="flex flex-col gap-8">

```html {all|4|5|6|all}
<a
class="btn"
href="https://ohmy.co"
target="_blank"
rel="noopener noreferrer external"
title="Visit ohmy.co"
>
Besök ohmy
</a>
```




<a class="btn" href="https://ohmy.co" target="_blank" rel="noopener noreferrer external" title="Visit ohmy.co">Besök ohmy</a>


<!-- <div class="abs-br p-4 text-xs opacity-50 hover:underline">
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a" >Link to MDM
</a>
</div>  -->
<!-- <div v-click="2" fade>(Search engines uses this attribute to get more info about a link)</div> -->

</div>
</div>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

---
layout: default
---

# `<a>` : [The Anchor element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)

<div grid="~ cols-2 gap-8">
<div>

The anchor element, with its href attribute, creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address.

Content within each `<a>` should indicate the link's destination.


</div>
<div class="flex flex-col gap-8">

<div class="relative">
<v-clicks>
```html {all|3}
<div class="wrapper">
    <a class="js-menu-handler" 
      href="javascript:;">
      <img src="/svg/hamburger.svg">
    </a>
</div>
```

<arrow  x1="310" y1="105" x2="200" y2="60" color="#FF0000" width="3" arrowSize="1" />
<div class="z-30 abs-br px-10 py-5 bg-[#FF0000] ">NEJ!</div>  
</v-clicks>
</div>







</div>
</div>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

---
layout: default
---

# `<nav>` : [Navigation Section element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)

<div grid="~ cols-2 gap-8" class="">
<div>

The `<nav>` HTML element represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.


</div>
<div class="flex flex-col gap-8">


```html 
<nav class="crumbs">
    <ol>
        <li class="crumb"><a href="#">Bikes</a></li>
        <li class="crumb"><a href="#">BMX</a></li>
        <li class="crumb">Jump Bike 3000</li>
    </ol>
</nav>
```

</div>
</div>
---
layout: default
---

# `<section>` : [The Generic Section element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)

<div grid="~ cols-2 gap-8">
<div>

 The `<section>` HTML element represents a generic standalone section of a document, which doesn't have a more specific semantic element to represent it. Sections should **always have a heading**, with very few exceptions..


</div>
<div class="flex flex-col gap-8">


```html 
<section>
    <h2>Introduction</h2>
    <p>This document provides a guide to help 
      with the important task of choosing 
      the correct Apple.</p>
</section>

<section>
    <h2>Criteria</h2>
    <p>There are many different criteria to be 
      considered when choosing an Apple —
      size, color, firmness, sweetness, tartness...</p>
</section>
```

</div>
</div>
---

# [The keyboard input element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd)

<div grid="~ cols-2 gap-8">
<div>

The `<kbd>` HTML element represents a span of inline text denoting textual user input from a keyboard, voice input, or any other text entry device.

|     |     |
| --- | --- |
| <kbd>cmd</kbd> + <kbd>r</kbd>| to refresh |


</div>
<div class="flex flex-col gap-8">

```html {all}
<kbd>cmd</kbd> + <kbd>r</kbd>to refresh 

```


</div>
</div>
---
layout: center
class: text-center
---

# Learn More

[mdm web docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) · [link to slides](https://html-presentation-carljohan.vercel.app/)
