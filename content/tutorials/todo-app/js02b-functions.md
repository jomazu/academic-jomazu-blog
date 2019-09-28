---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "JavaScript Functions"
summary: "Section 2b"
authors: [John Zukowski]
tags: [JavaScript, Functions]
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
## Requirements
Functions needed for building a `TODO` application:  

- [x] It should have a function (recipe) to **DISPLAY** todos  
- [x] It should have a function (recipe) to **ADD** todos  
- [x] It should have a function (recipe) to **CHANGE** todos  
- [x] It should have a function (recipe) to **DELETE** todos   

<br>
## DISPLAY
Create a function to **DISPLAY** todos.  

```javascript
// Enter todos variable array data
> var todos = ['item 1', 'item 2', 'item 3'];

// Create the displayTodos function
> function displayTodos() {
    console.log(`My Todos: ${todos}`);
  }

// Call the displayTodos function
> displayTodos();
My Todos: item 1,item 2,item 3
```

<br>
## ADD
Create a function to **ADD** todos.  

```javascript
// Enter todos variable array data
> var todos = ['item 1', 'item 2', 'item 3'];

// Create the addTodo function
// Add a todo parameter
// Add displayTodos function to output new addition
> function addTodo(todo) {
    todos.push(todo);
    displayTodos();
  }

// Call the addTodo function
> addTodo('item 98');
My Todos: item 1,item 2,item 3,item 98
```

In the `addTodo`, we used a concrete example about how to customize a function with a parameter, and how to use that parameter. Also, we used a function inside another function.

<br>
## CHANGE
Create a function to **CHANGE** todos.  

```javascript
// Enter todos variable array data
> var todos = ['item 1', 'item 2', 'item 3', 'item 98'];

// Create the changeTodo function
// Add a parameter for the index (position)
// Add a parameter for the new value (newValue)
// Add displayTodos function to output new addition
> function changeTodo(position, newValue) {
    todos[position] = newValue;
    displayTodos();
  }

// Call the changeTodo function
> changeTodo(3, 'item 4');
My Todos: item 1,item 2,item 3,item 4
```

The `changeTodo` example takes two parameters. The first parameter tells the function which item to change. The second parameter tells the function the new value that you want to set that item to. The `displayTodos` function is added inside `changeTodo` so that it displays the new `todos` array (list) after the change.  

<br>
## DELETE
Create a function to **DELETE** todos.  

```javascript
// Enter todos variable array data
> var todos = ['item 1', 'item 2', 'item 3', 'item 4'];

// Create the deleteTodo function
// Add a parameter for the index (position) to delete
// The number of items to delete is hardcoded as 1, so no parameter needed.
// Add displayTodos function to output new addition
> function deleteTodo(position) {
    todos.splice(position, 1);
    displayTodos();
  }

// Call the deleteTodo function
> deleteTodo(0);
My Todos: item 2,item 3,item 4
```

The `deleteTodo` function takes one parameter (position), to delete the item you want to get rid of at a specific position.  

<br>
## Review
The list below shows the functions learned and used in this section:  

1. Create an Array to `STORE` todos
```javascript
// Create a todos array
var todos = ['item 1', 'item 2', 'item 3'];
```
2. Create a Function to `DISPLAY` todos 
```javascript
// A function to DISPLAY todos.
function displayTodos() {
  console.log(`My Todos: ${todos}`);
}
```
3. Create a Function to `ADD` todos
```javascript
// A function to ADD todos.
function addTodo(todo) {
  todos.push(todo);
  displayTodos();
}
```
4. Create a Function to `CHANGE` todos
```javascript
// A function to CHANGE todos.
function changeTodo(position, newValue) {
  todos[position] = newValue;
  displayTodos();
}
```
5. Create a Function to `DELETE` todos
```javascript
// A function to DELETE todos.
function deleteTodo(position) {
  todos.splice(position, 1);
  displayTodos();
}
```
<br>
[Next page...](../js03-objects)