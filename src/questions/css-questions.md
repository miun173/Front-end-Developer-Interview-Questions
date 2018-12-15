---
title: CSS Questions
layout: layouts/page.njk
permalink: /questions/css-questions/index.html
---

* What is CSS selector specificity and how does it work?
  - specificiy is how browser decide which css property values are most relevant, it's based on css selector.
  - the browser decision based on the css selector weight, the most wieght will be applied as property.
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why? 
  - resetting: make an element unstyled
  - normalizing: make an element consistent accross browser
* Describe Floats and how they work.
  - floats make an element to the left or right of the container
  - floats define using keyword value
* Describe z-index and how stacking context is formed.
  - z index define how element position in z-axis with other element
  - the most value will make the element up higher in z-axis
* Describe BFC (Block Formatting Context) and how it works.
  - It define the regions of layout of block boxes and which floats interact with other elements
* What are the various clearing techniques and which is appropriate for what context?
  - Empty div method - <div style="clear:both;"></div>.
  - Clearfix method — Refer to the .clearfix class above.
  - overflow: auto or overflow: hidden method - Parent will establish a new block formatting context and expand to contains its floated children.
* How would you approach fixing browser-specific styling issues?
  - we can use different style rules to load for specific browser
  - use autoprefixer 
  - use framework/library that already solved these issues
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
    - Progressive enhancement — The practice of building an application for a base level of user experience, but adding functional enhancements when a browser supports it.
* What are the different ways to visually hide content (and make it available only for screen readers)?
  - visibility: the element is still in the page, and still takes up space.
  - width: 0; height: 0. not showing it.
  - position; absolute; left: -99999px. Position it outside of the screen.
  - text-indent: -9999px. This only works on text within the block elements.
* Have you ever used a grid system, and if so, what do you prefer?
  - bootstrap is good but i like to use my own flexbox or using css grid (vanilla css)
* Have you used or implemented media queries or mobile specific layouts/CSS?
  - yes, for most projects I developed, i go from mobile first layout on go up to desktop
* Are you familiar with styling SVG?
  - no
* Can you give an example of an `@media` property other than `screen`? 
  ```
  @media print {
  ...
  }
  ```
* What are some of the "gotchas" for writing efficient CSS? 
  - not every part of bootstrap will be used
  - we tend to use the same css rules more that once, it adds up bundle size
  - Sometimes the style differ from one browser to others
* What are the advantages/disadvantages of using CSS preprocessors?
  - props: many nice features: variables, nested selector, prefixing
  - cons: add tool chains for development, compiled it to single bundle sometimes make it not efficient for users
  * Describe what you like and dislike about the CSS preprocessors you have used.
    - I only work in CSS in JS, it was nice. I used styled-components
* How would you implement a web design comp that uses non-standard fonts?
  - Need to check the fonts license before using it in projects. 
* Explain how a browser determines what elements match a CSS selector. 
* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* What is the CSS `display` property and can you give a few examples of its use?
* What's the difference between inline and inline-block?
* What's the difference between the "nth-of-type()" and "nth-child()" selectors?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* Can you explain the difference between coding a web site to be responsive versus using a mobile-first strategy?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?
