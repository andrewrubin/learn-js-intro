# WTC Lunch & Learn: Intro to JavaScript

## Part 1: An Introduction

### What is Javascript
- A programming language, primarily used in web browsers.
- Created in ’95 by Brandon Eich, who was hired to do so, by the company that would become Mozilla (you may have heard of them).

### A brief terminology primer
- **event:** something that occurs in the web-browser—such as a click, scroll, or hover.
- **static:** This refers to content on a web page that is "hard-coded", or has data which is "set in stone", so to speak.
- **dynamic:** This refers to content on a web page which is not static or fixed. Something that is displayed programatically—based on user input, for example.
- **API:** This is an acronym for “Application Programming Interface”. An API can refer to any methodology that has been created to assist in programming with some codebase. For example, FedEx has created their own API, which we can leverage to retrieve information about shipping rates, based on user location. 

### What is JavaScript used for?
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

### Examples of JavaScript's usefulness
- **A _to-do list_ component**
  - The following example (comprised of `1.1`, `1.2`, and `1.3`) illustrates the _evolution_ of a component—from HTML to CSS to JavaScript.
  - **Example 1.1** - static HTML: https://codepen.io/andyranged/pen/f7ce88815ce544cfa91b780abec90a93
  - **Example 1.2** - adding some CSS styling: https://codepen.io/andyranged/pen/657c499a997345d6c4756cfbb80c384c
  - **Example 1.3** - bringing the component to life with JavaScript: https://codepen.io/andyranged/pen/a5778886dc0c35230e0e52f0ddf660bf
    - Not only does **Example 1.3** show how JS brings interactivity to a component; it also illustrates how data is stored and retrieved based on user input. You can see the data being manipulated with each add/remove/reverse action, from within the `console`.
- **Consuming data**
  - The following example illustrates a common scenario, in which a developer is given a massive chunk of data, and is tasked with "parsing" that data into something nice and readable.
  - **Example 2** - Working with large sets of data: https://codepen.io/andyranged/pen/24f51ec8e60c5e9a1914af30a0feef62

## Part 2: Hands-on

Any code snippets you see here are intended to be copied and pasted into your CodePen editor (in the JavaScript pane). Please edit the examples provided, and try to come up with your own variations on the examples where possible!

### Some basics
- Intro to the `console` object
  - Using `console.log()` to get feedback from our code.
  - (Note: this bullet point is intended to be _super basic_, and is just here for the purpose of seeing feedback from what we do. No need to explain what an object or a method is yet).
    ```js
    console.log('Hello world!');
    console.log('My name is Andrew.');
    ```
- **Primitive data types**
  - Most important for this lesson: **string**, **number**, and **boolean**
    - **Strings** are sequences of characters wrapped in quotes (single or double, just be consistent).
      - Escape character: `\` is used to "ignore" what would be a closing quote. Example: `'I heard Sarah\'s cat is larger than Jeff\'s dog'`. If we don't _escape_ the apostrophes, the first one would cause our string to end, which would in turn trigger utter CATastrophy.
    - **Numbers** are what they sound like - just _not_ wrapped in quotes. `"5"` is a string, while `5` is a number.
    - **Booleans** are one of two values—either `true` or `false`.
  - Other data types you'll come across: **undefined**, **null**.
  - You can use the `typeof` operator to check the type of any value. Here, we'll use it to confirm that strings and numbers are indeed different data types:
    ```js
    console.log(typeof "5");  // -> outputs "string" to the console
    console.log(typeof 5);    // -> outputs "number" to the console
    ```
- **Arithmetic operators**
  - `+`, `-`, `*`, `/`
  - Others: `%`, `**`, `++`, `--`
  - Note that the normal mathematical "order of operations" applies here: Parenthesis --> Exponents  --> Multiplication / Division --> Addition / Subtraction.
  - Here are some examples of basic arithmetic in JavaScript:
    ```js
    console.log(5 + 5);           // 10
    console.log(150 - 10)         // 140
    console.log(4 * 4)            // 16
    console.log(4 / 2 * 6 - 10)   // -2
    ```
- **Concatenation**
  - The addition operator (`+`), when used on a string, becomes the "concatenation" operator. This is used to "glue" strings onto one another.
    ```js
    console.log("Andrew" + "Rubin");
    // AndrewRubin

    console.log("Hello there. " + "What are you doing in my kitchen?");
    // Hello there. What are you doing in my kitchen?
    ```
  - What happens when you try to add a string to a number, or vice versa?
    - When you write the expression `5 + "5"`, JavaScript detects that you're adding a string to a number. The string—being a string—will instead be concatenated onto the number. In this instance, you'll get the result `"55"`, rather than the expected "10".
    - If you were to ask JavaScript to evaluate `5 + 5 + "10"`, JS would add the two numbers, and then concatenate the string onto the end. So in this case, instead of spitting out "20", you'd get `"1010"` (the result of 5 + 5, then "10" contatenated onto it).

- **Comparison operators and booleans** `==`, `===`, `!=`, `!==`, `<`, `>`, `<=`, `=>`
  - equal `==` compares **value**
  - strict equal `===` compares **value** _and_ **type**
  - not equal `!=` checks if values are _not_ the same
  - strict not equal `!==` checks if values and types are not the same.
  - greater than `>` and less than `<` compare the value of numbers.
  - greater than or equal to `>=` and less than or equal to `<=` compare the value of numbers.
  - All of the above (if used properly—to compare two items) will return boolean values (true or false).
  ```js
  console.log(20 == 20);      // true   (same value)
  console.log(20 == "20");    // true   (same value)
  console.log(20 === 20);     // true   (same value AND data type. Both are of type "number".)
  console.log(20 === "20");   // false  (same value, different data type)

  console.log(35 > 20);       // true
  console.log(35 >= 35);      // true
  console.log(50 <= 24);      // false
  console.log(20 != 10);      // true
  ```

### Variables
- **What is a variable?**
  - A variable can be thought of as a label, to which you can _bind_ (assign) values.
- **Why would you want to use a variable?**
  - Variables are part of the essence of any programming language. They allow you to store values—simple or complex—into a nice reference (or label) that you can pass around and reuse when you may need it.
- **Variable Declaration and assignment**
  - Variables are declared with the `var` keyword.
    - (there are other ways to declare variables, but for the purposes of this lesson, you should only be concerned with `var`).
    ```js
    var name;
    var hairColor;
    ```
  - Variables have somewhat strict naming rules—they must not start with a number, they must not contain spaces, and so on. It is common practice to name variables using camelCase or underscores: `petName`, or `pet_name`.
  - Variables are _assigned_ using the assignment operator, which is a single equals `=` sign:
    ```js
    var name = "Andrew";
    var hairColor = "blond";
    var vision = 2020;
    ```
  - You will most often declare variables and assign them in the same line, as shown in the code block above.
  - Variables can be assigned any value—strings, numbers, booleans, functions, null, undefined, etc.

- **Using variables**
  - Here's an example in which we're concatenating some information together, pieces of which are stored in variables:
    ```js
    var name = "Gertrude";
    var message = "My name is " + name;

    console.log(message);     // "My name is Gertrude"

    var species = "human";
    var age = 106;
    var aboutMe = "I am a " + age + "-year-old " + species + ".";

    console.log(aboutMe);
    ```
  - In this next example, we will compare some variables:
    ```js
    var sisterAge = 24;
    var brotherAge = 17;

    console.log(sisterAge < brotherAge);              // false

    var player1_score = 18022;
    var player2_score = 9278;

    console.log(player1_score === player2_score);     // false
    console.log(player1_score > player2_score);       // true
    ```

### Conditionals
- If this, then that!
- Conditional statements (often referred to as "if statements", or "control flow"), are necessary for writing **logic** into your JavaScript programs.
- A basic `if` statement looks like this:
  ```js
  if (something is true) {
    then do something!
  }
  ```
  - Although the above snippet contains invalid code, the structure is what's important here.
- After the keyword `if`, between the two parenthesis, you'll input some kind of test or expression, which evaluates to either `true` or `false`. From here, JavaScript knows whether or not to run whatever code is between the curly brackets `{}`.
- Now that we understand the _format_ of an `if` statement, here's a real example:
  ```js
  if (10 > 5) {
    console.log("Yes!");
  }
  ```
  - In the above example, the line of code `console.log("Yes!");` will run, because the test inside the parenthesis `()` evaluated to true.
  ```js
  if ("dog" == "cat") {
    console.log("You learn something new every day.");
  }
  ```
  - In the above example, nothing will happen! This is because the expression between the parenthesis evaluates to false. Thus, the code inside the `{}` block will never run. (the string "dog" is not the same value as the string "cat").

- **else, and else if**
  - What if you want something to happen if the condition is not met (i.e. the test is false)?
  - Introduce the `else` clause:
    ```js
    if ("dog" == "cat") {

      console.log("*world explodes*");

    } else {

      console.log("Yep, no new information here.");

    }
    ```
  - Simply add the keyword `else` after the closing curly bracket of your statement, and open up a new pair of curly brackets for whatever code you want to run if the initial condition is _not_ met.
- **else if**
  - If you want to get even more specific with controlling the flow of the user experience, you can add extra tests onto your if statement, using the keyword `else if`:
    ```js
    var questionsCorrect = 12;
    var totalQuestions = 19;
    var resultMessage = "You answered " + questionsCorrect + " out of " + totalQuestions + " questions correctly. ";

    if (questionsCorrect <= 7) {

      console.log(resultMessage + "Keep on training.");

    } else if (questionsCorrect <= 14) {

      console.log(resultMessage + "You'll be a Pokémon master in no time!");

    } else {

      console.log(resultMessage + "You're a true Pokémon master!");

    }
    ```
  - Note that as soon as one of these conditions are met, the code corresponding to that condition will execute, and JavaScript will abort going through the rest of the if statement. Be careful how you organize your `else if`s!

- **Logical operators**
  - Logical operators allow us to be more specific with our conditional statements.
  - The logical operators are:
    - "AND": `&&` - both expressions in the condition must be true
    - "OR": `||` - one of the expressions in the condition must be true
    - "NOT": `!` - negates an expression.
  - These operators can be used inside conditional statements:
    ```js
    var luckyNumber = 12;

    if (luckyNumber > 1 && luckyNumber < 10) {

      console.log("Your lucky number is probably seven.");

    } else if (luckyNumber >= 11) {

      console.log("Your lucky number could be anything. But it's definitely not 1 through 10.");

    } else if (luckyNumber === 0 || luckyNumber < 0) {

      console.log("Your lucky number is either zero, or negative :(");

    } else {

      console.log("You didn't enter a lucky number.");

    }
    ```

----

### Exercise: Greeting a user!

**Part 1:**

Create a program which does the following:
- Prompts a user for their name, and stores that value in a variable.
  - Tip: you can use the `prompt()` function to ask for user input.
  - You can then store that in a variable. For example:
    ```js
    var age = prompt('How old are you?');
    ```
  - It may help to turn off CodePen's auto-update feature for this exercise. You'll see why. **Settings > Behavior > Auto-Updating Preview**.
  
- Create a `message` variable which concatenates a message string onto the user's name.
- Display the personalized greeting in the console.

**Part 2:**

- In this same program, display a different message in the console, only *if* the user's name is Bowser.
  - Hint: you can _reassign_ variables… do what you will with that information!

**Part 3:**

- In this same program, check if the user has entered the number `11`, or the word `"Eleven"`, as their name.
  - If this is the case, let's display a unique message for them—maybe something _Stranger Things_-related. 🤓
  - There are multiple ways to do this. If you encounter an error, try "debugging" it by console-logging the user's name with the `typeof` operator discussed earlier.

- Finally, for everybody else, display a generic message.

----
