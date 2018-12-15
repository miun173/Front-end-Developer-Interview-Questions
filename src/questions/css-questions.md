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
  - using @font-face or @import
* Explain how a browser determines what elements match a CSS selector. 
  - Browsers match selectors from rightmost (key selector) to left
  - It filter out elements in the DOM according to the key selector, and traverse up its parent elements to determine matches.
* Describe pseudo-elements and discuss what they are used for.
  - A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s)
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
  - The CSS box model is responsible for calculating:
    - How much space a block-level element takes up.
    - Whether or not borders and/or margins overlap, or collapse.
    - A box’s dimensions.
  - The box model has the following rules:
    - The dimensions of a block element are calculated by width, height, padding, borders, and margins.
    - If no height is specified, a block element will be as high as the content it contains, plus padding (unless there are floats, for which see below).
    - If no width is specified, a non-floated block element will expand to fit the width of its parent minus padding.
    - The height of an element is calculated by the content's height.
    - The width of an element is calculated by the content's width.
    - By default, paddings and borders are not part of the width and height of an element.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
  - By default, elements have box-sizing: content-box applied, and only the content size is being accounted for.
  - box-sizing: border-box changes how the width and height of elements are being calculated, border and padding are also being included in the calculation.
  - The height of an element is now calculated by the content's height + vertical padding + vertical border width.
  - The width of an element is now calculated by the content's width + horizontal padding + horizontal borderwidth.
* What is the CSS `display` property and can you give a few examples of its use?
  - 
* What's the difference between inline and inline-block?
  - Inline-Block
    - Size — Depends on content.
    - Positioning — Flows along with other content and allows other elements beside.
    - Can specify width and height — Yes.
    - Can be aligned with vertical-align — Yes.
    - Margins and paddings — All sides respected.
  - Inline
    - Size — Depends on content.
    - Positioning — Flows along with other content and allows other elements beside.
    - Can specify width and height — No. Will ignore if being set.
    - Can be aligned with vertical-align — Only horizontal sides respected. Vertical sides, if specified, do not affect layout. Vertical space it takes up depends on line-height, even though the borderand padding appear visually around the content.
    - Margins and paddings — Becomes like a block element where you can set vertical margins and paddings.
* What's the difference between the "nth-of-type()" and "nth-child()" selectors?
* What's the difference between a relative, fixed, absolute and statically positioned element?
  - A positioned element is an element whose computed position property is either relative, absolute, fixed or sticky.
  - static - The default position; the element will flow into the page as it normally would. The top, right, bottom, left and z-index properties do not apply.
  - relative - The element's position is adjusted relative to itself, without changing layout (and thus leaving a gap for the element where it would have been had it not been positioned).
  - absolute - The element is removed from the flow of the page and positioned at a specified position relative to its closest positioned ancestor if any, or otherwise relative to the initial containing block. Absolutely positioned boxes can have margins, and they do not collapse with any other margins. These elements do not affect the position of other elements.
  - fixed - The element is removed from the flow of the page and positioned at a specified position relative to the viewport and doesn't move when scrolled.
  - sticky - Sticky positioning is a hybrid of relative and fixed positioning. The element is treated as relative positioned until it crosses a specified threshold, at which point it is treated as fixed positioned.
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
  - Bootstrap --> just pick the component I need and compiled it from Bootstrap website
  - Styled-Component --> not a framework but it's kind of CSS in JS. It allow's me to writing css like usual for React component
  - tachyonns --> it was kind of atomic css. It applies composition for making the UI, the class in tachyons are small and applicable. It aims to reduce repetition when using css
* Have you played around with the new CSS Flexbox or Grid specs?
  - Yes if using them
* Can you explain the difference between coding a web site to be responsive versus using a mobile-first strategy?
  - Responsive Website means making the UI looks right for different screen size
  - Mobile-first strategy is an approach to make Responsive Website by build from smaller screen (mobile) to larger (desktop)
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
  - nope
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?
  - translate() is a value of CSS transform. Changing transform or opacity does not trigger browser reflow or repaint, only compositions, whereas changing the absolute positioning triggers reflow
