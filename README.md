# The North Face Code Challenge 

The goal: output a standard landing page to showcase the North Face featured collections. 
Use a JS Object JSON response from the North Face API call from [this link](https://docs.google.com/document/d/1DkFjhdkO9BWfjctXP-63iY2oYHSKNLTgGeZUffCAKHw/edit).

## Overview

[The finished page](https://cweachock.github.io/the-north-face) presents a simplified full width design layout using a modern JS framework called [Handlebars js](https://handlebarsjs.com/) with some minimal styling. I mostly tried to focus on the implementation portion and exploring more of Handlebars to package the data. I used handlebars because I think it has a clean syntax, and it's easy to build, read, and maintain. There is also room for more complex conditional logic if there is a need. In addition, it's also easier to manage the HTML elements so the markup is kept separately from the JS. The build is hosted on [github](https://github.com) with [github pages](https://pages.github.com/). 

Content is run through a handlebars loop and iterated over using built-in helpers.  

### Looping through the Collections 

I thought the best way to present the data would be to iterate through it. Since handlebars has great helper functions I can just go down the list and call up each featured collection using a [block operator](https://handlebarsjs.com/block_helpers.html) from the JSON data. In this case, I stripped down the main.js to only show the JSON data to be read by Handlebars the best I could. The list of values for the images, titles, and link text is looped through and compiled with handlebars to then show a HTML page. 


```
{{#hits}} insert HTML styling here {{/hits}}

```

### Showing Content in the Loop

To show content in the loop I used the standard Handlebars expressions with the standard curly braces operators: {{}} wich references the JSON variable data in the file for each collection. This includes images, titles, text, and links. 

like so:

```
<h1>{{jcr:title}}</h1><a class="shopNowSmall" href="{{jcr:path}}"> Shop Now </a>

```

### Showing the Explore Fund Grant and Endurance Challenge

I thought it would be good to break up the loop by showing the additional elements after the first featured item in the collection. I used the built in operators @first and @last to conditionally show the Explore Grant Fund and the Endurance challenge callouts or promos. If statements were used to check which index we are on, then if we are on the selected index it shows the content (the Grant and the Challenge).  


```
{{#if @first}} insert some html stuff here {{/if}}
```


## Conclusion

The resulting was a low-level page that pulls the JSON data in a clean and simple way to show it on the frontend facing in HTML. I mostly tried to focus on the logic and implementation to pull the data from the API response in a way that could be re-templated. In addition, I tried to keep my CSS clean and small for the exercise. The CSS also uses vector widths, %'s, for responsiveness, and media queries at the smallest image resolution breakpoint which was 640px.    


