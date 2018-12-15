---
title: HTML Questions
layout: layouts/page.njk
permalink: /questions/html-questions/index.html
---

* What does a `doctype` do?
  - DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.
  
* How do you serve a page with content in multiple languages?
  - in React we can use `react-intl` 
  
* What kind of things must you be wary of when design or developing for multilingual sites?
   - The complexity of translation
   
* What are `data-` attributes good for?
  - an attribute is anything in html that can modify, or provide more information for, an element. So, href, alt, class, id, etc are all attributes. data-* is also an attribute, but the cool thing is that you aren't boxed in by what is already available, and where the * is you can add (kindof) whatever you might want.

* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
  - new form elements
  - new javascript API
  - new communication API
  - new css api

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
  - In terms of capabilities, cookies, sessionStorage, and localStorage only allow you to store strings 
  - it is possible to implicitly convert primitive values when setting (these will need to be converted back to use them as their type after reading) but not Objects or Arrays (it is possible to JSON serialise them to store them using the APIs). Session storage will generally allow you to store any primitives or objects supported by your Server Side language/framework.
  
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
  - Normal execution <script>
  This is the default behavior of the <script> element. Parsing of the HTML code pauses while the script is executing.
  
  - Deferred execution <script defer>
  delaying script execution until the HTML parser has finished.
  - Asynchronous execution <script async>
  HTML parsing may continue and the script will be executed as soon as it’s ready.

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
  - You usually put the <link> tags in between the <head> to prevent Flash of Unstyled Content which gives the user something to look at while the rest of the page is being parsed.
  - Since Javascript blocks rendering by default, and the DOM and CSSOM construction can be also be delayed, it is usually best to keep scripts at the bottom of the page.
  - Exceptions are if you grab the scripts asynchronously, or at least defer them to the end of the page.

* What is progressive rendering?
  - chunking the HTML into separate bits and loading each block as it's finished. 
  - usually, the backend code loads the HTML at once, but if you flush after finishing one part of the structure, it can be rendered immediately to the page.

* Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
  - You would use the srcset attribute when you want to serve different images to users depending on their device display width – serve higher quality images to devices with retina display enhances the user experience while serving lower resolution images to low-end devices increase performance and decrease data wastage (because serving a larger image will not have any visible difference).

* Have you used different HTML templating languages before?
  - yes: blade
