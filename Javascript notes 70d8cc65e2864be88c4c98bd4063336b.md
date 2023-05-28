# Javascript notes

## **variable**

 varibale is a named storage for a data.We can use variables to store goodies, visitors, and other data.

**There are** **4 Ways to Declare a JavaScript Variable:**

- Using `var`
- Using `let`
- Using `const`
- Using nothing

If  a general rule is needed: always declare variables with `const`.

If  the value of the variable can change, use `let`.

It is recommended we use `let` instead of `var`. However, there are a few browsers that do not support `let`. 

**JavaScript Identifiers**

All JavaScript **variables** must be **identified** with **unique names**.

These unique names are called **identifiers, javaScript identifiers are case-sensitive.**

Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).

The general rules for constructing names for variables (unique identifiers) are:

- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter.
- Names can also begin with $ and_.
- Names are case sensitive (y and Y are different variables).
- Reserved words (like JavaScript keywords) cannot be used as names.

**Change the Value of Variables**

It's possible to change the value stored in the variable. For example,

```
// 5 is assigned to variable x
let x = 5;
console.log(x); // 5

// vaue of variable x is changed
x = 3;
console.log(x); // 3
```

## **operator**

is a special symbol used to perform operations and operands.

there are different types of operators :-

- Assignment Operators : used to assign values to variables.
- Arithmetic Operators: used to perform arithmetic calculations.
- Comparison Operators: used to compare two values and return a boolean value,either true or false.
- Logical Operators: used to perform logical operations and return a boolean value and also used in decision making and loops.
- Bitwise Operators: perform operations on binary representations of numbers.
- String Operators:
- Other Operators: , ? delete.. etc…

## **primitive and non-primitive data types**

![Untitled](Javascript%20notes%2070d8cc65e2864be88c4c98bd4063336b/Untitled.png)

**JavaScript primitive data types:** are data types that refer to a single value.

**E.g. `var a =5;`**

Here the variable ‘a’ is an integer data type and has a single integer value. The variable ‘a’ refers to a single value in memory. If we want to change the value of a, we would have to assign a new value to a. 

 *Primitive data types are not mutable.*

When we create a variable, it reserves a space for itself in the memory. The variable ‘a’ has space in memory which holds its value. When we try to change the value of ‘a’ by assigning another value like var a = 6, it doesn’t alter the value of the original a, it just creates a new variable ‘a’ with the new value 6.

We can assign the value of ‘a’ to another variable like this:

**`var a1=a;`**

Here the variable ‘a1’ is assigned the value of ‘a’, not the address of ‘a’ in memory.

Thus ‘a1’ now holds the same value as ‘a’.

We can compare the two variables ‘a’ and ‘a1’ as the two variables refer to the same value now.

Using the comparison operator will return a Boolean value of ‘true’.

**`a===a1 // equals to ‘true’ as ‘===’`**  checks both the value and type of these two variables are true.

JavaScript non-primitive types are objects, Arrays and Functions in JavaScript belong to the ‘object’ data type.  An object holds a reference/address of a single key-value pair or many key-value pairs. Whenever we refer to an object, we refer to an address in memory which contains the key-value pair. If we assign an object ‘object1’ to another object ‘object2’, we are actually assigning the address of ‘object1’ to ‘object2’ instead of the key-value pair which the ‘object1’ contains in memory. Let’s see below”.

**`var object1= {a:5, a1:6};`**

**`var object2 = object1;`**

When we compare these two objects, we find that both of them refer to the same address in memory.

object1===object2 //will return true, as both refer to the same address. If we compare two separate objects like below:

**`var object1= {a:5, a1:6};`**

**`var object2 = {a:5, a1:6};`**

This statement object1===object2 // would return a false because both the objects refer to two separate addresses in memory. When we compare two objects, we compare their addresses, not their values.

We have seen above in case of primitive data types, that when we assign the variable ‘a’ to variable ‘a1’, the value of ‘a’ is copied to ‘a1’, and not its address which happens in non-primitive data types.

Thus primitive data types refer to a ‘single value’ in an address in memory whereas non-primitive data types refer to the ‘address’ in memory which contains single or multiple key-value pair/s.

## **Data structure**

data structure is ****a format to organize, manage and store data in a way that allows efficient access and modification.

JavaScript has **primitive (built in)** and **non-primitive (not built in)** data structures.

Primitive data structures come by default with the programming language and we can implement them out of the box (like arrays and objects). 

Non-primitive data structures don't come by default and we have to code them up if we want to use them.

Different data structures exist because some of them are better suited for certain kind of operations. the most popular data structures are:

### **Arrays**

An array is a collection of items stored at contiguous memory locations.

Each item can be accessed through its **index** (position) number. Arrays always start at index 0, so in an array of 4 elements we could access the 3rd element using the index number 2.

The **length** property of an array is defined as the number of elements it contains. If the array contains 4 elements, we can say the array has a length of 4.

In JavaScript, arrays come with many built-in properties and methods we can use with different purposes, such as adding or deleting items from the array, sorting it, filtering its values, know its, length and so on.

When we add a new item at the end of the array, it just takes the index number that follows the previous last item in the array.

But when we add/delete a new item **at the beginning or the middle** of the array, the **indexes** of all the elements that come after the element added/deleted **have to be changed**. This of course has a computational cost, and is one of the weaknesses of this data structure.

Arrays are useful when we have to store individual values and add/delete values from the end of the data structure. But when we need to add/delete from any part of it, there are other data structures that perform more efficiently.

### **Objects (hash tables)**

In JavaScript, an **object** is a collection of **key-value pairs**. This data structure is also called **map**, **dictionary** or **hash-table** in other programming languages.

A typical JS object looks like this:

```
const obj = {
    prop1: "I'm",
    prop2: "an",
    prop3: "object"
}
```

Objects can store both values and functions. When talking about objects, values are called properties, and functions are called methods.

```
const obj = {
    prop1: "Hello!",
    prop3: function() {console.log("I'm a property dude!")
}}
```

To access properties you can use two different syntaxes, either `object.property` or `object["property"]`. To access methods we call `object.method()`.

```
console.log(obj.prop1) // "Hello!"
console.log(obj["prop1"]) // "Hello!"
obj.prop3() // "I'm a property dude!"
```

Like arrays, in JavaScript objects come with many built-in methods that allow us to perform different operations and get information from a given object.

Objects are a good way to group together data that have something in common or are somehow related.

### **Stacks**

Stacks are a data structure that store information in the form of a list. They allow only adding and removing elements under a **LIFO pattern (last in, first out)**. In stacks, elements can't be added or removed out of order, they always have to follow the LIFO pattern.

### **Queues**

Queues work in a very similar way to stacks, but elements follow a different pattern for add and removal. Queues allow only a **FIFO pattern (first in, first out)**. In queues, elements can't be added or removed out of order, they always have to follow the FIFO pattern.

### **Linked lists**

**Linked lists** are a type of data structure that store values in the form of a **list**. Within the list, each value is considered a **node**, and each node is connected with the following value in the list (or null in case the element is the last in the list) through a **pointer**.

There are two kinds of linked lists:-

**singly linked lists:-** in singly linked lists each node has a **single pointer** that indicates the **next node** on the list.

 **doubly linked lists:-** each node has **two pointers**, one pointing to the **next node** and another pointing to the **previous node**.

### **Trees**

Trees are a data structures that link nodes in a **parent/child relationship**, in the sense that there're nodes that depend on or come off other nodes.

## Control flow

 in JavaScript is how your computer runs code from top to bottom. It starts from the first line and ends at the last line, unless it hits any statement that changes the control flow of the program such as loops, conditionals, or functions. In this article, I’m going to be explaining these three statements more in depth, and how they affect control flow.

### **Loops**

Loops are iteration statements that will keep running until there is either nothing left to loop over, or if the condition becomes false. There are many types of loops in JavaScript, but for now I’m going to be going over three of them. Let’s start with the most common used one, the `for` loop. The `for` is a conditional loop, which means that it runs based on if a certain condition is true. As long as it stays true, the code is going to keep executing.

### The For Loop

The `for` statement creates a loop with 3 optional expressions:

for (*expression 1*; *expression 2*; *expression 3*) {  // *code block to be executed*}

**Expression 1** is executed (one time) before the execution of the code block.

**Expression 2** defines the condition for executing the code block.

**Expression 3** is executed (every time) after the code block has been executed.

```
const edm = ['House', 'Dubstep', 'Drum and Bass']for (let i = 0; i < edm.length; i++) {
 console.log(edm[i])
}// 'House'
// 'Dubstep'
// 'Drum and Bass'
```

The syntax for a `for` loop contains a variable declaration of `i` which is the index of the array `edm` that we are currently iterating over.

### **While Loop**

The `while` loop is similar to the `for` loop because it also runs *while* a condition is true. The difference between them is that you would use a `for` loop when you already know how many times you want the loop to be executed. A `while` loop is used when you are unsure about how many times the loop wants to run.

```
const edm = ['House', 'Dubstep', 'Drum and Bass']while (edm.length > 0) {
 const genre = edm.pop()
 console.log(genre)
}// 'Drum and Bass'
// 'Dubstep'
// 'House'
```

### **Do-while Loop**

Very similar to the `while` loop, this loop also runs on a `while` condition. However, it executes the condition after the fact.

```
const edm = ['House', 'Dubstep', 'Drum and Bass']
let i = 0do {
 console.log('I love dancing to' + edm[i])
 i++;
} while (i < 3);//'I love dancing to House'
//'I love dancing to Dubstep'
//'I love dancing to Drum and Bass'
```

## **Conditionals**

Conditional statements are implemented when you need to perform different actions based on different conditions. We recently used conditional type logic in the loops that we implemented, but conditionals are different from what we were just working with. In JavaScript, the conditional statements that we have are `if`, `else if`, `else`, and `switch` statements.

### **If, Else If, Else**

The `if` statement is used when we want a block of code to be run as long as the condition it true. Like so:

```
if (4 * 4 = 16) {
 console.log('This will run!')
}// 'This will run!'
```

This code will always print `'This will run!'` because 4 * 4 is always going equal 16. Let’s say we were writing something a little more complex, and wanted to log some code based on a different condition if the first one is false. That’s where `else if` comes in! This condition runs when the condition before it is false.

```
const hungryFor = ['pizza', 'sushi', 'french fries']for (let i = 0; i < hungryFor.length; i++) {
  if (hungryFor[i] === 'pizza') {
   console.log('I\'m hungry for ' + hungryFor[i])
} else if (hungryFor[i] === 'french fries') {
   console.log('But ' + hungryFor[i] + ' are also tasty!')
 }
}// 'I'm hungry for pizza'
// 'But french fries are also tasty!'
```

In this example, we iterated through the `hungryFor` array and had two conditionals inside it stating that if the index of the `hungryFor` array equaled `'pizza'`, then log a specific string. In this case, only the strings `'pizza'` and `'french fries'` were printed. `'sushi'` wasn’t because it never met the conditionals requirements. If we wanted to set a default value to this `if` statement, then we would have to use `else` . The `else` condition only runs if everything before it is false.

```
const hungryFor = 'sushi' if (hungryFor === 'pizza') {
  console.log('I will not print')
} else if (hungryFor === 'french fries') {
   console.log('I will not print')
} else {
   console.log('But I will :)')
}// 'But I will :)'
```

Since the variable `hungryFor` is equal to just one string, the first two conditions are both false, so the `else` code block only runs.

### **Switch**

Switch statements serve the same purpose as `if` statements, however, they have their share of differences. `switch()` first takes in an expression and evaluates it once. If any of the preceding cases match the expression, then the return statement within that case will be executed.

```
function getDayOfTheWeek(num) {
 switch (num) {
  case 1:
   return 'Monday';
  case 2:
   return 'Tuesday';
  case 3:
   return 'Wednesday';
  case 4:
   return 'Thursday';
  case 5:
   return 'Friday';
  case 6:
   return 'Saturday';
  case 7:
   return 'Sunday';
 }
}console.log(getDayOfTheWeek(4))// 'Thursday'
```

## **Functions**

Functions are blocks of code that can be called by other code, by itself, or by a variable that refers to that function object. Usually when you call a function, it takes in one or multiple arguments and it can optionally return a value. We can take our previous examples from above, apply them to functions, and see how that affects the control flow of the application.

```
const edm = ['House', 'Dubstep', 'Drum and Bass']const hungryFor = ['pizza', 'sushi', 'french fries']
function printGenres(arr) {
 for (let i = 0; i < edm.length; i++) {
  console.log(edm[i])
 }
}function printFoods(arr) {
 for (let i = 0; i < hungryFor.length; i++) {
  console.log(hungryFor[i])
 }
}printFoods(hungryFor)
printGenres(edm)// 'pizza'
// 'sushi'
// 'french fries'
// 'House'
// 'Dubstep'
// 'Drum and Bass'
```

In this example, we have two functions that both do the same thing. This code isn’t very DRY obviously, however I did this purposely to show you how the control flow is affected. Even though the function `printGenres()` is declared first in the code, the second function is the first one being called. So as your code is executing, it sees that there are two functions, but will only run them when they’re eventually called. In this case, the second function `printFoods()` was the **first one called**, so it will be executed first.

All of these statements that were covered affect control flow because they essentially pause everything else that's happening until those conditions are met and everything to the possible extent could be executed.

## Classes

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on [prototypes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain) but also have some syntax and semantics that are unique to classes.

Classes are in fact "special [functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)", and just as you can define [function expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function) and [function declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function), a class can be defined in two ways: a [class expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/class) or a [class declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/class).

`// Declaration
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}

// Expression; the class is anonymous but assigned to a variable
const Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};

// Expression; the class has its own name
const Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};`

**class body**

The body of a class is the part that is in curly brackets `{}`. This is where you define class members, such as methods or constructor.

**Constructor**

The `[constructor](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/constructor)` method is a special method for creating and initializing an object created with a class. There can only be one special method with the name "constructor" in a class — a `[SyntaxError](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError)` is thrown if the class contains more than one occurrence of a `constructor` method.

A constructor can use the `[super](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super)` keyword to call the constructor of the super class.

You can create instance properties inside the constructor:

`class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}`

**Methods**

Methods are defined on the prototype of each class instance and are shared by all instances. Methods can be plain functions, async functions, generator functions, or async generator functions. For more information, see [method definitions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions).

`class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  // Getter
  get area() {
    return this.calcArea();
  }
  // Method
  calcArea() {
    return this.height * this.width;
  }
  *getSides() {
    yield this.height;
    yield this.width;
    yield this.height;
    yield this.width;
  }
}

const square = new Rectangle(10, 10);

console.log(square.area); // 100
console.log([...square.getSides()]); // [10, 10, 10, 10]`

**Static methods and fields**

The `[static](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/static)` keyword defines a static method or field for a class. Static properties (fields and methods) are defined on the class itself instead of each instance. Static methods are often used to create utility functions for an application, whereas static fields are useful for caches, fixed-configuration, or any other data that don't need to be replicated across instances.

`class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }

  static displayName = "Point";
  static distance(a, b) {
    const dx = a.x - b.x;
    const dy = a.y - b.y;

    return Math.hypot(dx, dy);
  }
}

const p1 = new Point(5, 5);
const p2 = new Point(10, 10);
p1.displayName; // undefined
p1.distance; // undefined
p2.displayName; // undefined
p2.distance; // undefined

console.log(Point.displayName); // "Point"
console.log(Point.distance(p1, p2)); // 7.0710678118654755`
Copy to Clipboard

**Field declarations**

With the class field declaration syntax, the [constructor](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes#constructor) example can be written as:

`class Rectangle {
  height = 0;
  width;
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}`