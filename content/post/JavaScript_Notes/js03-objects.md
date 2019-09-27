---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "JavaScript Objects"
summary: "Section 3"
authors: [John Zukowski]
tags: [JavaScript, Objects]
categories: [JavaScript, Objects]
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
[Objects](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics) are used in JavaScript to group related data and functions together.  

Example of an object related to my computer.  
```javascript
// Example object data with 3-properties
operatingSystem mac
screenSize 15 inches
purchaseYear 2015

// Above data transformed into JS object
// Assign the JS object to a variable (i.e. myComputer)
// Property: 'value',
// No ending comma needed after the last property value
// End the object notation with a semi-colon
> var myComputer {
    operatingSystem: 'mac',
    screenSize: '15 inches',
    purchaseYear: 2015
  };

> myComputer
{operatingSystem: "mac", screenSize: "15 inches", purchaseYear: 2015}

// Use dot notation to get a specific property value
> myComputer.operatingSystem
"mac"

> myComputer.screenSize
"15 inches"

> myComputer.purchaseYear
2015
```


## Objects and Functions
The relationship between objects and functions.  
Note, you can actually place functions on objects.  

Example, using an object that refers to itself, using [this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this).  

- `this`  

Note, there is no need to use the function name (i.e. `function sayName()` etc.), because the function shown below knows to use the `sayName` property as the function name.  

```javascript
> var john = {
    name: 'John',
    sayName: function() {
      console.log(`Hi, ${this.name}`);
    }
  };

> john.sayName();
Hi, John
```

To recap the example above...  

We have a JS object set to the variable name `john` with two properties:  

- `name` - set to *text*  
- `sayName` - set to a *function* that prints the name from our object. It is refering to that object as `this` (i.e. john).  

Remember, when used in a function that is sitting on an object (`this`) will refer to the object itself. So, in the example, `this` is refering to the `john` object, and uses `.name` to access the property on the object. Thus, `this.name` will equal the value `John`.  

This pattern of putting a function on an object is a very common practice. It is so common, that there is a name for this, it's called a [METHOD](https://developer.mozilla.org/en-US/docs/Glossary/Method).  

A **METHOD** is simply a property that is equal to a function.  

In our example above, `sayName` is actually a **METHOD** on the `john` object.  

Lastly, when you have a function on an object, you do not have to give it a name, because the way the function is called is with the `property name`. 

This is referred to as an **ANONYMOUS FUNCTION**.  


## Plunker
- `Login`  
- `Launch the Editor`  
- Select `script.js` from the Files section  
- Enter a `Description` to name the file:  
  - `PJS - V3` - PJS for "Practical JavaScript Version 3"  
- `Save`  
