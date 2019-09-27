---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "JavaScript Objects"
summary: "Section 3b"
authors: [John Zukowski]
tags: [Objects]
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
# Requirements
Version 3 requirements (To Do application):  

- It should **STORE** the todos array on an object  

*Place the following methods on an object that represents a Todo list*  
This helps to organize our code and ensure that everthing related to a Todo list is on a Todo list object.  

- It should have a **displayTodos** method   
- It should have an **addTodo** method  
- It should have a **changeTodo** method  
- It should have a **deleteTodo** method  


## STORE
**STORE** the `todos array` on an `object`.  

Go to Plunker and open `PJS - V3` and select `script.js`...  

Enter the following:  
```javascript
var todoList = {
  todos: ['item 1', 'item 2', 'item 3']
};
```

- `save` on Plunker  
- `run` on Plunker  
- Right-click and click inspect  
- Open the `console` tab and select the `top` dropdown and select `plunkerPreviewTarget`  

Now, you can access the Plunker data inside of your `PJS - V3` program.  


## displayTodos
Change the `displayTodos` function from a standalone function to a method on our `todoList` object.  

Previously created standalone function shown for context only:  
```javascript
function displayTodos() {
  console.log(`My Todos: ${todos}`);
}
```

Within Plunker, add the new `displayTodos Method` (anonymous function) to the `todoList` object:  
```javascript
displayTodos: function() {
  console.log(`My Todos: ${this.todos}`);
}
```

The `todoList` object should now look like such...  
```javascript
var todoList = {
  todos: ['item 1', 'item 2', 'item 3'],
  displayTodos: function() {
    console.log(`My Todos: ${this.todos}`);
  }
};

> todoList.displayTodos();
My Todos: item 1,item 2,item 3
```


## addTodo
Change the `addTodo` function from a standalone function to a method on our `todoList` object.  

Previously created standalone function shown for context only:  
```javascript
function addTodo(todo) {
  todos.push(todo);
  displayTodos();
}
```

Within Plunker, add the new `addTodo Method` (anonymous function) to the `todoList` object:  
```javascript
addTodo: function(todo) {
  this.todos.push(todo);
  this.displayTodos();
}
```

The `todoList` object should now look like such...  
```javascript
var todoList = {
  todos: ['item 1', 'item 2', 'item 3'],
  displayTodos: function() {
    console.log(`My Todos: ${this.todos}`);
  },
  addTodo: function(todo) {
    this.todos.push(todo);
    this.displayTodos();
  }
};

> todoList.displayTodos();
My Todos: item 1,item 2,item 3

> todoList.addTodo('item 4');
My Todos: item 1,item 2,item 3,item 4
```


## changeTodo
Change the `changeTodo` function from a standalone function to a method on our `todoList` object.  

Previously created standalone function shown for context only:  
```javascript
function changeTodo(position, newValue) {
  todos[position] = newValue;
  displayTodos();
}
```

Within Plunker, add the new `changeTodo Method` (anonymous function) to the `todoList` object:  
```javascript
changeTodo: function(position, newValue) {
  this.todos[position] = newValue;
  this.displayTodos();
}
```

The `todoList` object should now look like such...  
```javascript
var todoList = {
  todos: ['item 1', 'item 2', 'item 3'],
  displayTodos: function() {
    console.log(`My Todos: ${this.todos}`);
  },
  addTodo: function(todo) {
    this.todos.push(todo);
    this.displayTodos();
  },
  changeTodo: function(position, newValue) {
    this.todos[position] = newValue;
    this.displayTodos();
  }
};

> todoList.changeTodo(0, 'plunker');
My Todos: plunker,item 2,item 3
```


## deleteTodo
Change the `deleteTodo` function from a standalone function to a method on our `todoList` object.  

Previously created standalone function shown for context only:  
```javascript
function deleteTodo(position) {
  todos.splice(position, 1);
  displayTodos();
}
```

Within Plunker, add the new `deleteTodo Method` (anonymous function) to the `todoList` object:  
```javascript
deleteTodo: function(position) {
  this.todos.splice(position, 1);
  this.displayTodos();
}
```

The `todoList` object should now look like such...  
```javascript
var todoList = {
  todos: ['item 1', 'item 2', 'item 3'],
  displayTodos: function() {
    console.log(`My Todos: ${this.todos}`);
  },
  addTodo: function(todo) {
    this.todos.push(todo);
    this.displayTodos();
  },
  changeTodo: function(position, newValue) {
    this.todos[position] = newValue;
    this.displayTodos();
  },
  deleteTodo: function(position) {
    this.todos.splice(position, 1);
    this.displayTodos();
  }
};

> todoList.deleteTodo(0);
My Todos: item 2,item 3
```


## Success is a Process
Make sure to read Gordon Zhu's guide for asking questions:  
- [How to be great at asking coding questions](https://medium.com/@gordon_zhu/how-to-be-great-at-asking-questions-e37be04d0603)  
