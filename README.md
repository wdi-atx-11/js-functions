<!--
Creator: <Cory Fauver>
Market: SF
-->

![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# JavaScript Functions

### Why is this important?
<!-- framing the "why" in big-picture/real world examples -->
*This workshop is important because:*

Functions are the building block of programs. They are the conceptual unit that will help you transition to thinking like a developer. To think like a developer, begin to think in small tasks that achieve progress one by one. Write a function that performs each of these tasks and make them work together to achieve the larger result. Once you've divided the task into functions, you can just ask the function to perform its task repeatedly with different inputs to get different desired outputs.

### What are the objectives?
<!-- specific/measurable goal for students to achieve -->
*After this workshop, developers will be able to:*

- identify the differences between defining a function and calling a function (casting the spell).
- create a simple function that prints a value (for the user/developer to see a result) and a simple function that returns a value (for the rest of the code to use a result). Distinguish between the impact of these different results.
- draw a model of a function that includes arguments as input, side effects, and return values as output.
- begin to explain the concepts of scope and `this` in JavaScript.

### Where should we be now?
<!-- call out the skills that are prerequisites -->
*Before this workshop, developers should already be able to:*

- write their own JavaScript in a `.js` file and link that file to their HTML (with a `<script>` tag).
- explain the concept *flow of control* and it's role in running a piece of code.
- demonstrate understanding of string, number, and boolean data types in JavaScript.


# Setup

1. Summon the Chrome Developer Console (Option + Command + I)
1. Navigate to the `Sources` tab in the Chrome Developer Console.
2. Click on the `Snippets` tab within the Sources display.
3. Right-click and choose `New` to create a new Snippets file.
4. Name the Snippets File `myFunctions`.



![Ice Cream Sandwich Machine](https://media.giphy.com/media/1kowbKFzLQqXu/giphy.gif)

<em>A **function** is similar to a machine in that it receives an input (ice cream and cookies), processes the input (smash!), and creates a resulting output in a consistent manner (tasty ice cream sandwiches).</em>

![image](https://cloud.githubusercontent.com/assets/6520345/17683207/d55e5fda-6305-11e6-93e2-fdd72a87f81a.png)

# What is a Function?
A function can be thought of as a program within a larger program.  They often perform small or repetitive tasks.  


## Benefits of Using Functions

- **Encapsulation** - Keeping code for the same purpose in the same place makes finding it and updating it easier.

- **Code Reuse** - "Don't Repeat Yourself" (DRY) is a principle of coding - keep your programs DRY! Reusing code makes it easier to change how your program works, since you only have to make updates in one place. If you find yourself writing the same code two or more times, a good rule of thumb is to move it into a function!


### Examples of functions:

- Accept cell phone numbers as input and output (return) the state that phone number comes from.
- Accept credit card numbers as input and output (return) the credit card company that is associated with the card.
- Accept a string (words, letters, or any type of text) as input and output (return) the same string with all of the A's capitalized.

Once you have **DEFINED** the function you can then repeatedly **CALL** the function to use it over and over.

The function below will display the message `'Hi, everyone!'` to a console.

```javascript
    // function definition
    function greetEveryone() {
        // anything inside the curly braces will be executed
        console.log('Hi, everyone!');
    }
```

The above code is called a *function definition*.  On its own, the function will not execute. The function definition is simply the recipe for "the spell."  The function will need to be *called* by an outside source to initialize and carry out its tasks. You need to "cast the spell" for it to have an impact on the context around it.  To call a function, type the function name and trailing parenthesis as a statement.

```javascript
    // function call
    greetEveryone(); // In the console, you'll see 'Hi, everyone!'
```

When a function is *called*, the code from within the definition's curly braces (these -> **`{}`**) will be executed.  It will only be executed when the function is called.


# Defining a function with a parameter
When a function receives a parameter, it will use that value to perform an action. In the function `greetPerson(name)` the function requires that a name value be given to it.  

```javascript
    // function definition
    function greetPerson(name) {
        console.log('Hello ' + name);
    }
```

Similar to calling a function without parameters, the function name is called as a statement.  Parameters are passed into the function within the parenthesis.

```javascript
    // function call
    greetPerson('Andrea') // The console will print the string 'Hello Andrea'
    var firstName = 'Jeff';
    // function call
    greetPerson(firstName); // The console will print the string 'Hello Jeff'
```

### Say hello to some students
Functions can take variables as parameters or Strings

```javascript
    var name1 = 'Christopher';
    var name2 = 'Judy';
    var name3 = 'Noomi';

    // function calls
    greetPerson(name1); // The console will print the string 'Hello Christopher'
    greetPerson(name2); // The console will print the string 'Hello Judy'
    greetPerson(name3); // The console will print the string 'Hello Noomi'

    greetPerson('Will'); // The console will print the string 'Hello Will'
```

## Functions with Return Values
The above functions use `console.log()` to display a message to the screen. `console.log()` is a function for *giving information to the developer* - it shows evidence that something has happened wherever the developer wants to see evidence.

Functions also have the ability to *give information to the code* for later use. To do this, we use `return` statements.

```javascript
    // square a number and return the new value
    // function definition
    function square(a) {
      return a * a;
    }

    // function call      |
    //                    V
    var mySquaredValue = square(8);
    console.log(mySquaredValue); // 64
```
The particular function above multiplies the input value by itself and *returns* (gives) the resulting product to the line where it was called.  The variable `mySquaredValue` now stores the *return* value that the function call `square(8)` output. In this case, the `=` sign is called *assignment*. It assigns a value (whatever value is returned from `square(8)`) to a variable name, `mySquaredValue`. We can then use `mySquaredValue` to refer to that value anywhere in the code instead of needing to call the function over and over again. This is nice, because eventually we'll write much longer functions that we won't want to execute over and over again for fear of eating up processing power.

## Defining a function with multiple parameters

Functions can take multiple paramters.  Each parameter must be separated from another by a comma.  

```javascript
   	// Add two integers
    // function definition
    function sum(a, b) {
        console.log(a + b);
    }

    var x = 6;
    var y = 2;

    // function calls
    sum(x, y); // 8
    sum(2, 3); // 5
    sum(44, 33); // 77
```

## Functions on Integers
```javascript
    // Subtract two integers
    function subtract(a, b) {
        console.log(a - b);
        return a - b;
    }
```
``` javascript  
    // Multiply two integers
    function multiply(a, b) {
        console.log(a  *  b);
        return a * b;
    }
```
```javascript
    // Divide two integers
    function divide(a, b) {
        console.log(a / b);
        return a / b;
    }
```

How would you call the above functions?

But what if you want to perform functions on numbers that aren't integers?!  Don't worry; Javascript lumps integers and decimal numbers together in one `number` data type, so your functions will still work if you give them arguments that aren't whole numbers.


## Functions on Strings
Functions may perform actions upon Strings as well.

```javascript
    // convert String to uppercase

    // function definition
    function shout(phrase) {
        console.log(phrase.toUpperCase());
    }

    var phrase = 'i am mighty.'
    // function call
    shout(phrase); // I AM MIGHTY.
```
```javascript
    // convert String to lowercase

    // function definition
    function whisper(phrase) {
        console.log(phrase.toLowerCase());
        return phrase.toLowerCase();
    }

    //function call
    whisper('I AM SMALL'); // prints and returns the string 'i am small'
```

```javascript
    // append an exclamation point to the end of a phrase

    //function definition
    function exclaim(phrase) {
        console.log(phrase + '!');
        return phrase;
    }

    var phrase = 'Avast, ye mateys';
    // function call
    exclaim(phrase); // prints and returns the string 'Avast, ye mateys!'
```

**Note:** When naming Javascript functions, it is best practice to
 use camelCase if multiple words are used in the title.
 This helps with readability, much like the case with
 variable and file naming conventions.

> **Bad Naming (doesn't follow convention):**
>
> * `Squarethesenumbers()`
> * `CONVERTTOBINARY()`
> * `pythagoreantheorem()`
>  
> **Good Naming (follows convention):**
>
> * `hexToBinary()`
> * `determineRootVariant()`
> * `deployPhaserTorpedos()`

```javascript
    // convert spaces to dashes in a phrase

    // function definition
    function spacesToDashes(phrase) {
        console.log(phrase.replace(/ /g, "-"));
        return phrase.replace(/ /g, "-");
    }

    var phrase = "Dash is also a great API lookup tool!";
    // function call
    spacesToDashes(phrase); // prints and returns 'Dash-is-also-a-great-API-lookup-tool!'
```

In the case of the function spacesToDashes, the name describes the function and is in lowerCamelCase (first word not capitalized, other words capitalized with no spaces).



##Functions on Booleans
Functions are able to receive and return boolean values.  Functions that return boolean values are commonly used to check the states of variables and whether conditions are met.

> **Note:** It is best practice to name functions with boolean return values with a prefix of 'is', 'has', or 'can.'
>
> * isEven()
> * isPrime()
> * hasCheezburger()
> * canItBlend()
>
> This will let the programmer know that the return value of the function will be a boolean value.  It also increases the readiblity of the code.

### Function with boolean value as a parameter
```javascript
// outputs a statement based on boolean value
function hasCheezburger(answer)){
    if (answer === true) {
        console.log("Can I haz ur Cheezburger?");
    } else {
        console.log("Y no Cheezburger?");
    }
}
var answer = true;
hasCheezeburger(answer); // Can I haz ur Cheezburger?
```

### Function with boolean return value
```javascript
// checks if number is greater or less than 5
function isGreaterThanFive(number){
    if(number > 5) {
        return true;
    } else {
        return false;
    }
}

var number = 3;
var result = isGreaterThanFive(number);
console.log(result); // false;
```
The above function has two return statements.  Since both are within an `if / else ` statement, only one will apply to the condition.  Once a return statement is executed the function ends.  This ensures that only one return statement can be executed per function.  

*A function may have multiple possible return statements but only one may be executed at any one given function call.*

### Function with both boolean parameter and return values

```javascript
// return opposite boolean value of parameter received
function completelyDisagree(option) {
    if (option === true) {
        return false;
    } else {
        return true;
    }
}

var iAmRight = true;
var doYouAgree = completelyDisagree(iAmRight);
console.log(doYouAgree); // false
```


Examples of functions:
- input a cell phone number and output the name of state it's from.
  function definition:
  ```js
    function cellNumberLocator(cellNumber){
      var location;
      // pick off the area code of the phone number given
      // that is, find the first three digits of cellNumber
      // refer to an API of area codes to find the related state
      return location;
    }
  ```
  function calls:
  ```js
    cellNumberLocator(5055882300);
    var jennysHomeState = cellNumberLocator(2028675309);
  ```
- input a credit card number and output the name of the credit card company that it comes from.
  function definition:
  ```js
    function determineCardCompany(creditCardNumber){
      var cardCompany;
      // take the first four digits of creditCardNumber;
      // refer to a table that associates those four digits with card companies
      // and store the company name using the variable cardCompany;
      return cardCompany;
    }
  ```
  function calls:
  ```js
    determineCardCompany(4321000011112222);
    var myCardCompany = determineCardCompany(3400111122223333);
  ```

## Function Scope
A variable that is declared outside a function definition is a **global** variable, and its value is accessible and modifiable throughout your program. A variable that is declared inside a function definition is **local**.

Functions can access and modify global variables at will.  A program cannot access a function's local variable, however.  By nature, variables declared and defined within a function are created and destroyed as soon as the function starts and stops.  The local variable's data would be impossible to depend on from a source outside of the function.  

```javascript
/* banana is a global variable and can be accessed by all functions within the file */
var banana = 1;

/* This function will change the global variable `banana` */
function sliceBanana(slices){
    banana = slices;
    return;
}

sliceBanana(4);
console.log(banana) ;
=> 4
=> undefined
```

```javascript
function multiplyBySix(x){
    /* mult is a local variable and can only be accessed and altered within the function */
    var mult = 6;
    x = x * mult;
    return x;
}

console.log(multiplyBySix(4));
=> 24

/* Attempting to display a local variable outside of its scope will return an undefined */
console.log(mult);
=> Uncaught ReferenceError: mult is not defined!!! So Bad!!!!
```



## The Call Stack

We say that a function **takes in arguments** and **returns** something to us. You can imagine JavaScript control flow as a person talking on the phone with your program. When you call a function, it's like JS puts the main program on hold and contacts the function. If another function is called, JS puts the first function on hold to contact the new one. When the function finishes, JS returns to the previous call.

To keep track of the functions JS has on hold, it uses a **call stack**. As JS calls a new function, it pushes the function onto the call stack. When a function returns, it pops that function off of the call stack.

![](http://i.stack.imgur.com/4Z6xK.png)


## Function Recursion

Function recursion is the act of a function calling itself within its own code.  Traditionally, *recursive* functions require at least one parameter passed in.  Each time a function calls iself, the value of the parameter is changed to produce a desired effect.

```javascript
/* Display all numbers from num to 0 on the screen */
function countDown(num){
    /* Base Case */
    if(num < 0){
        return;
    } else {

        /* Action Steps */
        console.log(num);
        num = num - 1;

        /* Recursive Steps */
        countDown(num);     
    }
}

countDown(10);
=> 10 9 8 7 6 5 4 3 2 1 0
```

### What is this magic?!
1.  The code above displays the current value of `num` to the screen then decrements the value by one.  
2.  It then calls `countdown(num)` again. This time the value has been decremented.  
3.  Notice that these statements are encapsulated inside an `if` statement.  This creates what is known as a *base case*.  
4.  When `num` no longer satisfies the conditional statement `num >= 0`, (the variable reaches zero,) the function will no longer call itself and will end.
5.  Pat yourself on the back.  This is not simple stuff!  


![recursion](https://lh3.googleusercontent.com/-BOYdZI6tT7Y/UJwzRKYdQNI/AAAAAAAC5js/Ltg-gd6SCQQ/w506-h405/photo.jpg)

*Recursion is your friend!*


**Code Challenge:** Modify the above program to count down to zero, *then* count back up to the original value.



## Independent Practice
Refine the skills covered in this workshop with these [Function Exercises](https://github.com/SF-WDI-LABS/functions-exercises)

## Closing Thoughts
- review objectives & hierarchy of importance
- look ahead & link to future workshops
- clarify expectations and what developers should know by now
- reiterate “the why” with a perspective of your intentions
- create an active recall
- Check for understanding

## Additional Resources
- [External Resource](#)
