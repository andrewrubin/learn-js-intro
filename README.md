# WTC Lunch & Learn: Intro to JavaScript

## What is Javascript
- A programming language, primarily used in web browsers.
-   Created in ’95 by this dude (insert silly Brandon Eich gif here), who was hired to do so, by the company that would become Mozilla (you may have heard of them).


## A brief terminology primer
- **event:** something that occurs in the web-browser—such as a click, scroll, or hover.
- **dynamic:** This refers to content on a web page which is not static or fixed. Something that is displayed programatically, as opposed to being “hard-coded” HTML.
- **API:** This is an acronym for “Application Programming Interface”. An API can refer to any methodology that has been created to assist in programming with some codebase. For example, FedEx has created their own API, which we can leverage to retrieve information about shipping rates, based on user location. 


## What is JavaScript used for?
- Spice-up boring old HTML!
- Add feedback and flare to user interactions
- Animation
  - Keep users engaged
  - Enhance user interactions with animations and transitions.
- Show/hide content based on conditional information. Examples:
  - If a user clicks a “login” button, then show a login modal window.
  - If a user only needs one more item in their cart in order to receive free shipping, display an appropriate call-to-action.
- Consume and manipulate data (examples):
  - A “to-do” list. Data must be stored and maintained somehow, when items are added and removed from the list.
  - Send and receive data from 3rd parties. Examples: dynamically pull in Tweets, shipping rates, or user information (My Nintendo).
- Tracking your users' behaviour, in an effort to provide marketing/strategy insight.
- And a whole lot more!


## Part 1

### Examples of JavaScript's usefulness
- **A _to-do list_ component**
  - Discuss the basic evolution of a component, from HTML to CSS to JS.
  - Example 1.1 - static HTML: https://codepen.io/andyranged/pen/f7ce88815ce544cfa91b780abec90a93
  - Example 1.2 - adding some CSS styling: https://codepen.io/andyranged/pen/657c499a997345d6c4756cfbb80c384c
  - Example 1.3 - bringing the component to life with JavaScript: https://codepen.io/andyranged/pen/e43f7b694367ad8c89bb6093ba057fba
  - Not only does this **Example 1.3** show how to bring interactivity to a component; it also illustrates how data is stored and retrieved based on user input. You can see the data being manipulated in the `console` here:


## Part 2

### Some basics
- Intro to the `console` object
  - Using `console.log()` to get feedback from our code.
  - (Note: this bullet point is intended to be _super basic_, and is just here for the purpose of seeing feedback from what we do. No need to explain what an object or a method is yet).
- Primitive data types
  - Most important for this lesson: `string`, `number`, `boolean`
  - Others you'll come across: `undefined`, `null`
  - Using the `typeof` operator to confirm that strings and numbers behave differently (`"5"` vs. `5`).
- Arithmetic operators
  - `+`, `-`, `*`, `/`
  - Others: `%`, `**`, `++`, `--`
- Demonstrate some basic arthmetic
  - What happens when you try to add a string to a number, or vice versa?
- Comparison operators and booleans; `==`, `===`, `!=`, `!==`, `<`, `>`, `<=`, `=>`
- Introduce **concatenation**

### Variables
- What is a variable? Why use one?
- Variable declaration and assignment.
- Using variables in the wild

### Conditionals
- The `if` statement, and more boolean talk.
  - actual use case for comparison operators
- Logical operators: `&&`, `||`, `!`
- `else`
- `else if`

----

### Exercise: Greeting a user!

**Part 1:**

Walk them through creating a short program which does the following things:
- `prompt()` a user for their name, and store that value in a variable.
- Create a `message` variable which concatenates a message string to the user's name.
- Display the personalized greeting in the console (or even `alert()` it just for fun. FUN!)

**Part 2:**

Display a different message only *if* the user's name is Andrew.

----

## Part 3

### Data Structures
- What is a data structure, and why would we need one?
- Arrays
  - Used for storing data in a particular order
  - Creating an array (literal)
  - Access an item within an array (mention zero-based index)
  - Common array methods: `Array.length`
- Objects
  - Used for storing data by name or *property*, in no particular order
  - Creating an object (literal)
  - Access a property of an object - only show dot notation for now.
  - (won't worry about explaining methods quite yet)

### Loops
- **What:** Repeat one or more task(s) a specified number of times.
- **Why:** Cut down repetitive code!
- Introduce the `while` loop
  - Simple example: couting down from 10, and outputting something to the console for each number.
- You can actually loop over the items of an array as well, using `Array.length` as your counter's starting point.
  - Show how to use a "counter" variable (`i`, from previous `while` loop example) to access an item in an array.
  - (Give an intriguing example. Loop over some cats or something).
  - Explain why this is so powerful.

### Functions
- **What:** The backbone of JavaScript. Used to create reusable blocks of code.
- **Why:** So you don't repeat yourself! This makes for nicer, more readable, and more reusable code.
- Function declaration and invocation
  - (examples)
- The `return` keyword
- Parameters and arguments

----

### Exercise: TBD

**Part 1:**

some stuff here

**Part 2:**

some more stuff here

----