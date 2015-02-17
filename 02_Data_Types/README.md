### Data Types in JavaScript and a few other basics

This is a pretty subjective and incomplete list of features of JavaScript data types that I found noteworthy, with some examples to try out in the browser console. Most of this is based on Chapter 3 of "Professional JavaScript for Web Developers" by N. Zachas, and some on "Effective JavaScript" by D. Herman. 

#### Variables 

One of the most important characteristics of JavaScript is that its variables are *loosely typed*. When defining and initialising a variable you don't need to declare its type. Also, types can sometimes be implicitly converted, for example the Boolean *true* can become the Number *1*. This makes the language very flexible, but can also lead to confusion.

To define a variable we use the operator *var*:
```javascript
var message = "Hello world!";
```

Once defined, the variable is referenced without the *var*:
```javascript 
message = 100
``` 
What we have done here, is reassign the variable to a different value. We change the value of the *message* variable and also its type (from String to Number). In many other languages the latter is not possible. 

#### 5 Simple (or Primitive) Data Types

There are 5 so-called primitive data types in JavaScript. *Everything else* is an object. The simple data types are:
- Undefined
- Null
- Boolean
- Number
- String

#### Checking for the Type

You can check what type a variable is by using the *typeof* operator:

```javascript
typeof "Today is pancake day!";    // "string"
typeof 1001;                        // "number"
typeof null;                        // "object"   hugh?

```

#### Undefined and Null

If a variable is defined, but not initialised (no value assigned to it), it will be of type *undefined*
```javascript
var message; 
typeof message;    // "undefined" 
```
A null value is an empty object pointer. It can be useful initialising a variable with the value null, if it is later to hold an object. I just mention this for completeness, for the moment I think it is not that relevant.

#### Boolean

The Boolean type can have two values: *true* or *false* (lowercase!)

Every value can be converted to a Boolean. Explicitly this is done by calling Boolean(), but it also happens implicitly, for example when *==*, *!=* or simply *!* (which means "is not") are used. 

**Try this in the console**
```javascript
var message = "Pancake day!";
if(message) {alert("Value is true");}

// Then set message to an empty string
var message = "";
if(message) {alert("Value is true");}   
// No alert will show up, because message is now 'falsy'

// Try:
if(!message) {alert("Value is 'falsy'");}
// Now an alert should pop up
```
#### Number

Some languages have different types for integers and floats, not so JavaScript. There is only one Number type. Beware of the inaccuracy of floats. For calculations try to convert them to integers. 

**Try this in the console**
```javascript
0.2 + 0.3 
0.1 + 0.2 
(0.1 + 0.2) + 0.3
0.1 + (0.2 + 0.3)

// Type in these numbers and press enter
070
0xA
```

There is one special numeric value worth mentioning: *NaN*. This stands for "not a number". For example, diving by 0 returns NaN, while this would throw an error in other languages. NaN has the strange characteristic that it does not equal itself!

```javascript
NaN == NaN      // false
```
Therefore, if you want to check if a value is NaN, you cannot do something like x == NaN. There is a function, *isNaN()* that can be used instead. 

```javascript
alert(isNaN(NaN)); 			//true
alert(isNaN(10));			//false - 10 is a number
alert(isNaN(“10”));			//false - can be converted to number 10
alert(isNaN(“blue”));		//true - cannot be converted to a number
alert(isNaN(true));			//false - can be converted to number 1
```

Another function worth mentioning: *parseInt()* This is very helpful when you want to make sure that a value is treated as an Integer. See in the example below.

Fun with implicit coercions:

**Try this in the console**
```javascript
"5" - 3
"5" + 3
parseInt("5") + 3  
"5" - "4"
"5" + "5"
"foo" + + "foo"
```

Try to always make sure that a value has the desired type. 

#### String

This data type does not need any introduction anymore, because we have already used it a lot! Strings are defined by putting the value in double or single quotes. You can concatenate string with the *+* operator. Any value can be converted to a string with the *toString()* method

#### Equal does not equal equal 

Much more could be mentioned if you wanted to go through the basics of the JavaScript language. We need control structures like *if()* and loops - *for, while* etc.. We are not looking at these now, they can easily be looked up, probably more easily than the data types. Or get familiar with them through [Codecademy](http://www.codecademy.com/)

Another thing we need is operators. There are the common +, -, * and / operators and some more, which we will come across when working through examples. And here again, Codecademy is your friend, if you want to become familiar with them. I mainly wanted to show the data types, because they have some quite unexpected characteristics.

One important concept is the different ways you can compare two values. You can use either == or === . When you use three equal signs that means you are checking that two values are not only identical in value, but are also of the same type.

**Try this in the console**
```javascript
"55" == 55      // true
"55" === 55     // false

```

Next, on to Functions..



















