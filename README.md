# The North Face Code Challenge 

The goal: output a standard landing page to showcase the North Face featured collections. 
Use a JS Object JSON response from the North Face API call from [this link](https://docs.google.com/document/d/1DkFjhdkO9BWfjctXP-63iY2oYHSKNLTgGeZUffCAKHw/edit).

## Overview

[The finished page](https://cweachock.github.io/the-north-face) presents a full width design using a modern JS framework called [Handlebars js](https://handlebarsjs.com/). And some minimal styling with media quieries, vector widths, initiated through a separate JSON file using Handlesbars and Jquery. I used handlebars because I think it had clean syntax, and it's easy to build, read, and maintain. There is also room for more complex conditional information if there is a need. It's all compiled through into a javascript function.  It's also easier to manage HTML elements so markup is kept separately. The build is hosted on [github](https://github.com) with [github pages](https://pages.github.com/). 

Content is run through a handlebars loop and iterated over using built-in helpers and styles with minimal CSS.

### Looping through the Collection 

Collections are shown using the each block operator through a JSON file. In this case, I stripped down main.js to only show the JSON data to be read by Handlebars. The list of values for the images, titles, and link text is looped through and compiled with handlebars to then show a HTML page. 


```
{{#hits}} insert HTML styling here {{/hits}}

```

### Showing Content in the Loop

The content is shown using expressions with the standard curly braces operators: {{}}. Which contain HTML, and text mixed with Handlebars expressions.  

like so:

```
<h1>{{jcr:title}}</h1><a class="shopNowSmall" href="{{jcr:path}}"> Shop Now </a>

```

### Showing the Explore Fund Grant and Endurance Challenge

I use the built in operators @first and @last to conditionally show the Explore Grant Fund and the Endurance challenge callouts or promos. I use If statements to check which index we are on.   


```
{{#if @first}} insert some html stuff here {{/if}}
```


## Conclusion

The resulting was a low-level page that pulls the JSON data in a clean and simple way. For this challenge, I tried to focus on the logic and  implementation for the exercise to build a page in a sound way using my own experience and resources from [handlebarsjs.com](https://handlebarsjs.com), [stackoverflow](https://stackoverflow.com), and [github](https://github.com) The resulting was a low-level page that pulls the JSON data in a clean and simple way. For this challenge, I tried to focus on the logic and  implementation for the exercise to build a page in a sound way using my own experience and resources from [handlebarsjs.com](https://handlebarsjs.com), [stackoverflow](https://stackoverflow.com), and [github](https://github.com)


