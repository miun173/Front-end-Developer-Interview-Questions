---
title: General Questions
layout: layouts/page.njk
permalink: /questions/general-questions/index.html
---

* What did you learn yesterday/this week? 
  - I learn how event loop works
  - I learn react hooks (still not clicked)
  - I learn about Microservices 
* What excites or interests you about coding?
  - Coding is like solving puzzle and writing your mind into a working product. 
  - With coding, it's like we can make almost what we think
* What is a recent technical challenge you experienced and how did you solve it?
  - I'm tasked to implement a UI design for Chat App, and i used React JS + Styled Components to build it 
* When building a new web site or maintaining one, can you explain some techniques you have used to increase performance?
  - I used chorme lighthouse feature, to see the performance issues 
  - I try to fix the suggested part from lighthouse report 
* Can you describe some SEO best practices or techniques you have used lately?
  - Use the good markup structure
* Can you explain any common techniques or recent issues solved in regards to front-end security?
  - For SPAs using JWT considered increase security 
  - If we build the backend ouselve, we can use reverse proxy to avoid CORS issue
* What actions have you personally taken on recent projects to increase maintainability of your code?
  - Seperation of features is the most sensible for me, it allows us jump into the component feature without looking into seperate the css, html, js using React Js. I also want to try using Story Book, we can documentize the components behaviour
* Talk about your preferred development environment.
  - I'm using vscode, linux, zsh
* Which version control systems are you familiar with?
  - It's GIT
* Can you describe your workflow when you create a web page?
  - I try to make the layout `container` first, it can be a page or part of the page. 
  - When i see that a component can be shared i refactored it into `components` folder. 
  - For state management, It will always used for handling authentication, so it might good to add it in the early development phase
  - We test the app using chrome devtools
* If you have 5 different stylesheets, how would you best integrate them into the site?
  - Just using the stylesheets that used by the page
* Can you describe the difference between progressive enhancement and graceful degradation?
  - progressive enhancement: start from the baseline features and improve it overtime
  - graceful degradation: it provide fallback for users browser that cannot use the current standard
* How would you optimize a website's assets/resources?
  - for image we can compress it and using jpeg
  - for icons we can use svg's if it has different size for particular case
* How many resources will a browser download from a given domain at a time?
  - It's probably 4: html, css, js, image/video
  * What are the exceptions?
    - we can used js and lazy load the css, and image/video
* Name 3 ways to decrease page load (perceived or actual load time).
  - minimize
  - remove unsued code/comments
  - lazy load
* If you jumped on a project and they used tabs and you used spaces, what would you do?
  - just used the already setting if the codebase are large.
  - if the code still small, we can talk about the code styled
* Describe how you would create a simple slideshow page.
  -  use simple markup to list images. 
  - wrap the entire list with one div, we’ll call it slideshow. 
  - use CSS to default them to hidden. 
  - use JavaScript to get the divs, store them as an array, and make the first one visible. 
  - build simple navigation (and “previous” and “next” button for example), so when it clicked, it shows/hides the appropriate image. 
* If you could master one technology this year, what would it be?
  - js + node js, (typescript?)
* Explain the importance of standards and standards bodies.
  - The use of standards automatically makes every page you build genuinely cross-browser and cross-platform.
  - Standards allow backwards compatibility and validation since they are written to be compliant with older browser versions
* What is Flash of Unstyled Content? How do you avoid FOUC?
  - Actually it's a treade off to make when you want a fast page load time. We can avoid using @import
* Explain what ARIA and screenreaders are, and how to make a website accessible.
  - is a spec defining support for accessible web apps. It defines bunch of markup extensions (mostly as attributes on HTML5 elements), which can be used by the web app developer to provide additional information about the semantics of the various elements to assistive technologies like screen readers.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
  - CSS animation is simpler
  - Js animation is too hacky
* What does CORS stand for and what issue does it address?
   - Cross Origin Resource Sharing
  - Under the policy, a web browser permits scripts contained in a first web page to access data in a second web page, but only if both web pages have the same origin. An origin is defined as a combination of URI scheme, hostname, and port number.
* How did you handle a disagreement with your boss or your collaborator?
  - We negotiate it, and talk what is the problem and how we might to solve it.
* What resources do you use to learn about the latest in front end development and design?
  - medium, youtube, twitter links, email news letter
