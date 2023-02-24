# JavaReforcement ☕
This repo belong to a face-to-face course that I am providing to set of colleagues: Beyling, Fabricio

⚠ This repo is not about learning to program, this course 
is about learn Java and its syntax.

## What this repo course will cover?

- Setup enviroment (install JDK + IDE)
- Data Types
- Features And Architecture
- String and Printing
- Control Instructions: Assignment Operators
  - Conditional Statements
  - Loops
- Arrays and ArrayList
- Collection Framework
- Classes, Objects and methods
- Object-Oriented Programming: Inheritance
- Object-Oriented Programming: Polimorphy and interfaces
- Inner Classes
- Static and Final
- Packaging
- Exceptions Handling
- Multithreading
- Lambdas Expressions
- IO Streams
- Generics
- Date and Time API
- String, Characters and Regular Expressions
- Data Structure Basics
- Algorithms Techniques
  - Recursion
- Algorithms: Sorting and Searching (Basics)

### What next?
I have more incoming courses:
- Data Structure and Algorithms
- Introduction to Springframework
- React API's with Spring Boot
- Event-Driven Microservice with Spring Boot, Kafka and Elastic
- Apache Kafka - Real-time Stream Processing
- Microservice with Spring Cloud
- Multithreading,Parallel & Asynchronous
- Concurrency, Multithreading and Parallel


## Data Types 
In java we have 8 main primitive types: 

| Type    | Size    | Range | Default Value|
|---------|---------|-------|--------------|
 | boolean | 1 bit   | true or false | false|
 | byte    | 1 byte  | -128 to 127 | 0|
 | short   | 2 bytes | -32,768 to 32,767 | 0|
 | int     | 4 bytes | -2,147,483,648 to 2,147,483,647 | 0|
 | long    | 8 bytes | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | 0L|
 | float   | 4 bytes | 1.4E-45 to 3.4028235E38 | 0.0f|
 | double  | 8 bytes | 4.9E-324 to 1.7976931348623157E308 | 0.0d|
 | char    | 2 bytes | '\u0000' to '\uffff' | '\u0000'|

We also have non-primitive data types, for example: `String`, `Array` or any other classes.

### Working with Numbers

In java with devide primitive number types in two parts:

#### Integers
Integers are the same set of number you learned from high-school: we have negatives and positives, e.g. `{-∞,...,-2,-1,0,1,2,...,∞}`. So if you need to work we that set of numbers, in java you have these options: `byte`, `short`, `int` and `long`.
Depending on your needed you will use one or another.

```
Case I: Save a user age. 
```

If you make a little of sense you will realize that you can use even `byte` or `short`. `byte` because the older person ever was 122 years old (base on wiki). But if you think is very limit you can perfectly use `short` type,
and should not consider any higher number data type for this case.

```java
short age = 28;
```

#### Floating Point
Again Float numbers are the same of those number sets you learned in high-school, talking about rational and irrational sets. Example `PI`, `E`, `0.5`, `1/2`, etc.
But in computer we can not save values like that, so we need an own representation of those numbers, so we have **Float Numbers**. Example `3.1415` that belong to `PI`, `2.7182` for the constant `E`, `0.5` for the fragtion `1/2`, etc.

So in java we have two options to work with that set of numbers: `float` and `double`.

```
Case II: Save the an employee salary
```


```java
double salary = 2300.89d;
```

#### Type Casting 💪🏼

Something we can get some situations when we work with two different type of numbers and we have to solve that need. For doing that, we have two cases:

##### Widening Casting
This type of casting is automatically always the following flow: when the value to convert is smaller than the desired one.

```
byte => short => char => int => long => float => double
```

So base on the previous definition we can say that the following code is `automatic casting`

```java 
  int num = 12;
  double numDouble = num;
  
  System.out.println(num); // it will be: 12
  System.out.println(numDouble); // it will be: 12.0
```

As you can see we do nothing to cast the `numDouble`, so that proof the casting is automatic.

##### Narrowing Casting

This type of casting is the opposite of the **Widening Casting** and because of that, this type of casting need to be done manually. How we can do that? 

- Place a parentheses with the higher value inside them in front of the value you want to cast.

```java 
  double numDouble = 12.0d;
  int num = (int) numDouble;
  
  System.out.println(numDouble); // it will be: 12.0
  System.out.println(num); // it will be: 12
```

And with this we end our Java Data Types study! 