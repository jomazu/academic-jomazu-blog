---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "JavaScript Functions"
summary: "Section 2"
authors: [John Zukowski]
tags: [Functions]
categories: [JavaScript, Functions]
date: 2017-12-04T13:21:05-07:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
<br>
Functions are just recipes. Generally speaking, a function is a code snippet (subprogram) that can be called by other code, by itself, or a variable that refers to the function.  

When a function is called, arguments are passed to the function as input, and the function can optionally return an output.  

Using a recipe analogy, this would be the basic concept of a function to make a salami sandwich...  

```javascript
// The steps
makeSalamiSandwich
  Get one slice of bread.
  Add salami.
  Put a slice of bread on top.

// The function
  function makeSalamiSandwich() {
    Get one slice of bread;
    Add salami;
    Put a slice of bread on top;
  }

// Call the function
makeSalamiSandwich();
```


## Customizing Functions
- [Parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function) - the names of the arguments to be passed to the function.  

Using the same recipe analogy from above, we will adjust the steps to accomodate for customizing the Salami sandwich:  

```javascript
// The steps
makeSandwichWith ____
  Get one slice of bread.
  Add ____.
  Put a slice of bread on top.

// The function
  function makeSandwichWith(filling) {
    Get one slice of bread;
    Add filling;
    Put a slice of bread on top;
  }

// Call the function
makeSandwichWith(salami);
```

Conceptual example of customizing a function:  
```javascript
> function sayHiTo(person) {
  console.log(`Hi, ${person}`);
}

// Set the person variable to John
> sayHiTo('John');
Hi, John
```
