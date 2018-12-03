# Learning a new language

[Gist of examples](https://gist.github.com/DominicTremblay/95db442e4ff6c6d343b8616ed4468bd3)

When learning a new language, you learn about:

- Learn a new paradigm
- Learn a new framework
- Community behind the language

## Why Rails

- Learning a new language and framework
- Different approach to develop Web app
- Work with MVC pattern
- Coding with OO language
- A language/framework that makes your life easier

## Programming Paradigms

What is a programming paradigm?

A paradigm is a way of programming by following patterns

- Procedural
- Object-Oriented
- Functional

- The paradigm is a key charasteristic of a programming language
- Very few languages implement a paradigm 100%.
- multi-paradigm languages: language that supports more than one paradigms.

### Procedural programming

- imperative programming with procedures calls
- imperative programming means explicit sequence of steps in order for the computer to accomplish a particular task. We see how the task is done.
- what are procedures? functions that does't return a value
- the state is updated

#### problem with procedural programming?

- Applications grew in complexity over time
- Functions have unrestricted access to global data.
- This approach becomes inneficient and error-prone with larger projects
- Lots of dependencies throughout the program
- Tried a structured approach but did not work

ex. C, Go

```
const inventory = products => {
 let total = 0;
 for (let i = 0; i < products.length; i++) {
   if (products[i].category === "Electronics") {
     total += products[i].price * products[i].quantity;
   }
 }
 return total;
};
```

### Object Oriented Programming

#### Why OOP?

- As applications got more complex, they became very difficult to maintain.

#### What are the characteristics of OOP?

##### Principles of OOP

- Abstraction
- Encapsulation
- Inheritance
- Polymorphism (overriding)

* Base on objects. What are objects?
  - Abstraction of things we want to model
  - Objects have 2 parts: Properties (State) and Behaviors (Methods)
  - Intances of a class
* Class. What is a class?
  - A blueprint or a template for creating objects.

Ex. C++, Java, C#, Ruby

### Functional Programming

#### More Complexity

- Today Web applications are more complicated than back in the days
- As applications get bigger so their complexity

  - Async processes
  - Events firing
  - Complex user interface
  - Behave like native/mobile apps

Functional programming helps us to:

- Write more readable code (cleaner, less code, more modular)
- Produces code with less bugs

#### What is Functional Programming

- In FP we express everything with functions
- Code is declarative rather than imperative
  - Declarative code just state what the result should be, not how to do it (ex. map, filter functions)
- Functions do not change the state of our app and avoid producing side effects
- Functions should have a single purpose (singularity principle)
- Abstraction by using function composition

```
const inventory = products
 .filter(product => product.category === "Electronics")
 .map(product => product.quantity * product.price)
 .reduce((total, next) => (total += next), 0);
```

### JavaScript vs Ruby

- JS was created in 1995 in 10 days by Brendon Eich of Netscape
- JavaScript is multi-paradigms.

- Imperative coding
- Event-based programming
- Functional (JS was inspired by functional language such as LISP and Scheme)
  - support higher-order functions
  - support closures
- OOP (prototypal inheritance). It does not enforce OOP.

- Ruby was created by Yukihiro Matsumoto (Matz)
- Was designed for developer happiness and productivity
- Really took off with the release of Ruby on Rails (2005)
- Ruby is mostly OOP but can also do imperative programming and use FP concepts

Ex.: ReactJS follows a FP style of programming

## Domain of Applications

### Web Development

- JavaScript/Node/Express
- Ruby/Rails
- Python/Django
- Java/Spring
- C#/.net
- PHP / Laravel

### Data Science and Machine Learning

- Python
- R
- MathLab
- Scala
- Julia
- SQL
- JavaScript
- C/C++

### Internet of Things

- Assembly
- C/C++
- Go
- JavaScript
- Java
- Python
- PHP
- B#
- Swift

### Mobile

- Native

  - Java (Android)
  - Swift (IOS)
  - Objective-C (Legacy code on IOS)
  - C# (Windows)

- Hybrid
  - React Native (React)
  - Ionic (Angular)
  - PhoneGap (Apache/Cordova)
  - Framework 7 (JavaScript)
  - Xamarin (Microsoft)

## Running Context

- (Compiled? Interpreted? Platform-specific?)

  - Interpreted? The interpreter will execute each instructions at run time and transforming it into machine-code on the fly each time the program is run. Interpreted code is portable. More flexible when coding.
  - Compiled? The source code is compiled (tranformed into machine language), before being executed. This is more efficient than interpreted. It can run any number of times without overhead. This is machine specific.
  - Hybrid-approches: JIT Compilers => source code is compiled at run-time into byte-code (high-level marchine language) and then interpreted by a virtual-machine. JIT optimizes the code to run faster.

- JavaScript? Uses a JIT compiler
- Ruby? Ruby 2 is interpreted. Some flavors or Ruby have a JIT compiler. Starting in 2.6, Ruby should have a JIT Compiler (optional --jit flag)

## Does the language has an active community

- Support resources: documentation, tutorials, books, etc.

## How is the language typed

- JavaScript is loosely typed (JS types: string, boolean, number, null, undefined, symbol, object)
- Ruby is also loosely typed, but types are all objects
  (ex. "hello".class, 5.class, (123.123).class, true.class)

  JavaScript is:

- JavaScript is very flexible. it's a mixed-paradigm language. Most of the time imperative code. It can also be object-oriented and functional.
- JavaScript supports higher-order functions and closures.
- JavaScript does prototypal inheritance
- Javascript is an event-driven language.
- Tied to runtimes (e.g. Node, Browser) JIT compiling
- The only language supported in the browser.
- JavaScript is everywhere!
  Mobile applications, websites, web servers, desktop and embedded applications.
- JS community is:
- Chatty
  - Prolific
  - Open to talking about the craft at a low level.
  - Dynamic typing (AKA Weak typing)

Ruby is:

- OO first (With features for imperative/procedural & FP)
- In Ruby, everything is an object
- Ruby use Duck Typing
  - Treats objects according to the methods they define rather than the classes from which they inherit
- Runs on the Ruby Runtime (MRI Interpreter or CRuby)
- Ruby community:
  - Has a lot of language hobbyists
  - Has a lot of Rails devs (web use cases)
  - Pretty prolific (Probably a library for whatever you want to do)
  - Welcoming in culture

## A Few Surveys

- [Developer Survey Results
  2018](https://insights.stackoverflow.com/survey/2018/)
- [Tiobe Index](https://www.tiobe.com/tiobe-index/)
- [The State of JavaScript](https://stateofjs.com/)

## Ruby-style syntax

- JavaScript

```
function fizzBuzz(num){
  if(num % 3 === 0){
    if(num % 5 === 0){
      return 'FizzBuzz';
    }
    return 'Fizz';
  }
  if(num % 5 === 0){
    return 'Buzz';
  }
  return num;
}

console.log(fizzBuzz(4));
```

- Ruby

```
def fizz_buzz num
  if num % 3 == 0
    if num % 5 == 0
      'FizzBuzz'
    else
      'Fizz'
    end
  elsif num % 5 == 0
    'Buzz'
  else
    num
  end
end

puts fizz_buzz 4
puts fizz_buzz 3
puts fizz_buzz 5
puts fizz_buzz 15
```

### Differences

- no brackets, end instead
- no semi-colons
- implicit returns
- snake case instead of camel case
- omit parentheses
- no need for ===

### Ruby Data Types

All data types are objects based on classes.

- Booleans
- Symbols
- Integers
- Floats
- Strings
- Arrays
- Hashes

#### Strings

##### String Interpolation

- Same as with JavaScript except no need for back ticks and uses the # instead of \$

`"5 quarters makes #{ 5*0.25 } dollars"`

### Ruby Blocks

- Ruby blocks are anonymous functions that can be passed to methods
- Ruby blocks are similar to JavaScript callbacks

#### yield keyword

- yield will call the block

##### Ruby Iterators

- you need 2 things for iterators

  1. collection (arrays, hashes, ranges)
  2. block

- .each
- times
- upto, downto
- step

###### Arrays and Hashes

- Arrays and Hashes are collections
