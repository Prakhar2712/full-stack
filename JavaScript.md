# **INTRODUCTION TO JAVASCRIPT**

## 1. Console
The console is a panel that displays important messages, like errors, for developers. Much of the work the computer does with our code is invisible to us by default. If we want to see things appear on our screen, we can print, or log, to our console directly.

In JavaScript, the console keyword refers to an object, a collection of data and actions, that we can use in our code. Keywords are words that are built into the JavaScript language, so the computer will recognize them and treats them specially.

One action, or method, that is built into the console object is the .log() method. When we write console.log() what we put inside the parentheses will get printed, or logged, to the console.

It’s going to be very useful for us to print values to the console, so we can see the work that we’re doing.

```console.log(5); ```

This example logs 5 to the console. The semicolon denotes the end of the line, or statement. Although in JavaScript your code will usually run as intended without a semicolon, we recommend learning the habit of ending each statement with a semicolon so you never leave one out in the few instances when they are required.

You’ll see later on that we can use console.log() to print different kinds of data.

## 2. Comments
Programming is often highly collaborative. In addition, our own code can quickly become difficult to understand when we return to it— sometimes only an hour later! For these reasons, it’s often useful to leave notes in our code for other developers or ourselves.

As we write JavaScript, we can write comments in our code that the computer will ignore as our program runs. These comments exist just for human readers.

Comments can explain what the code is doing, leave instructions for developers using the code, or add any other useful annotations.

There are two types of code comments in JavaScript:

A single line comment will comment out a single line and is denoted with two forward slashes // preceding it.
```
// Prints 5 to the console
console.log(5);
```
You can also use a single line comment to comment after a line of code:
```
console.log(5);  // Prints 5 
```
A multi-line comment will comment out multiple lines and is denoted with /* to begin the comment, and */ to end the comment.
```
/*
This is all commented 
console.log(10);
None of this is going to run!
console.log(99);
*/
```
You can also use this syntax to comment something out in the middle of a line of code:
```
console.log(/*IGNORED!*/ 5);  // Still just prints 5 
```

## 3. Data Types
Data types are the classifications we give to the different kinds of data that we use in programming. In JavaScript, there are seven fundamental data types:

+**Number**: Any number, including numbers with decimals: 4, 8, 1516, 23.42.
+**String**: Any grouping of characters on your keyboard (letters, numbers, spaces, symbols, etc.) surrounded by single quotes: ' ... ' or double quotes " ... ". Though we prefer single quotes. Some people like to think of string as a fancy word for text.
+**Boolean: This data type only has two possible values— either true or false (without quotes). It’s helpful to think of booleans as on and off switches or as the answers to a “yes” or “no” question.
+**Null**: This data type represents the intentional absence of a value, and is represented by the keyword null (without quotes).
+**Undefined**: This data type is denoted by the keyword undefined (without quotes). It also represents the absence of a value though it has a different use than null.
+**Symbol**: A newer feature to the language, symbols are unique identifiers, useful in more complex coding. No need to worry about these for now.
+**Object**: Collections of related data.
The first 6 of those types are considered primitive data types. They are the most basic data types in the language. Objects are more complex, and you’ll learn much more about them as you progress through JavaScript. At first, seven types may not seem like that many, but soon you’ll observe the world opens with possibilities once you start leveraging each one. As you learn more about objects, you’ll be able to create complex collections of data.

But before we do that, let’s get comfortable with strings and numbers!
```
console.log('Location of Codecademy headquarters: 575 Broadway, New York City');
console.log(40);
```
In the example above, we first printed a string. Our string isn’t just a single word; it includes both capital and lowercase letters, spaces, and punctuation.

Next, we printed the number 40, notice we did not use quotes.


## 4. Arithmetic Operators
Basic arithmetic often comes in handy when programming.

An operator is a character that performs a task in our code. JavaScript has several built-in arithmetic operators, that allow us to perform mathematical calculations on numbers. These include the following operators and their corresponding symbols:

+Add: +
+Subtract: -
+Multiply: *
+Divide: /
+Remainder: %
The first four work how you might guess:
```
console.log(3 + 4); // Prints 7
console.log(5 - 1); // Prints 4
console.log(4 * 2); // Prints 8
console.log(9 / 3); // Prints 3
```
Note that when we console.log() the computer will evaluate the expression inside the parentheses and print that result to the console. If we wanted to print the characters 3 + 4, we would wrap them in quotes and print them as a string.
```
console.log(11 % 3); // Prints 2
console.log(12 % 3); // Prints 0
```
The remainder operator, sometimes called modulo, returns the number that remains after the right-hand number divides into the left-hand number as many times as it evenly can: 11 % 3 equals 2 because 3 fits into 11 three times, leaving 2 as the remainder.














