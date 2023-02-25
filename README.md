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


#### Another Cases

Another case you can face while learning is the arithmetic operations over those data types (Numerics). Imagine you have a `double` value, and you need to run an arithmetic operation with an `int` value.
The question here is: what data type will be the result of that operation?

So here is a table of those combinations:

| Type 1 | Type 2 | Resulting type |
|--------|--------|----------------|
| byte   | short  | int            |
| short  | int    | int            |
 | int    | long   | long           |
| long   | float  | float          |
| float  | double | double         |


And with this we end our Java Data Types study! 


### Working with truth values (Booelans)

Sometimes you will need to decide about things, and one data type that can help is the `boolean` data type, which can be `true` or `false` only.


```java
boolean isPremium = true;
boolean isOnline = false;
```

An important aspect of this data type is that can be created in combination of some `boolean expressions` that we will see soon.


## Strings

[String Documentation](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/String.html)

`String` class is custom data type, and I decided to talk about it in its own point **String and Printing** because is very special and the topic about it is a little interested.

**String** data type helps us to store text. Also is important (very important) to know that an `String` is build base on a collection of `character`s, but we can treat it as a single unit.
**String** data type is a class, and so we can create instances, so how we can create instance of a `String`?

### How to create String instances

#### Literales

You can create an `String` using double quotes, like:

```java
String street = "Carrer Moncada";
String name = "Benito Fuentes";
```

These variables are saved in memory as objects.

#### Constructor

```java
String someText = new String();
String street = new String("Carrer Moncada");
String anotherText = new String(street);
```

Do you remember we told `String` are a collection of `character`s?
So let's create an `String` using a collection of `character`s.

First of all a `character` is a data type and can be created using single quotes.

```java
char a = 'A';
char a = 65;
```
So let's build an `String` using `char`s:

```java
char[] charCollection = {'H', 'e', 'l', 'l', 'o'};
String helloText = new String(charCollection); // Output: Hello
```

### Concatenations

The concatenation operation is the action of join to different strings in one.

```java
String firstName = "Benito";
String lastName = new String("Fuentes");
String fullName = firstName + " " + lastName;
System.out.println(fullName); // Output: Benito Fuentes

fullName = firstName.concat(" ").concat(lastName);
System.out.println(fullName); // Output: Benito Fuentes
```

As you can see we can use `+` operator to join/concat two `String` in once, that we are saving in `fullName` variable.
But also we use `.concat` method, and this is possible because if you remember, we told `String` is a custom data type and also is a class that we can create instances by literals or its contructor.
If you take a time to read the documentation link I have putted for you, you will see a lot of ways for create an `String` and also a lot of methods we can use by accessing to it by the instance.

### Strings are immutable

`String`s are immutable as the class does not provide any method to modify the content of an `String` after this is created. This mean that once the `String` is created the characters that it contains can not be modified.
So let's check an example to be in mind and avoid confusion while you code and don't get the expected result:

```java
String name = "Benito";
name.concat(" Fuentes");
System.out.println(name); // Output: Benito
```

This example return 'Benito' because `String` are immutable and there is not any method on it to modify its content.

```java
String name = "Benito";
System.out.println(name.hashCode()); // Output: 1986181209

name=name.concat(" Fuentes");
System.out.println(name.hashCode()); // Output: -260495741
```

The `.hashCode` method is that return a identifier that is stored in the instance of the class. And as we can see we get a new instance of the string instead of a modified version.


### StringBuilder

[StringBuilder Documentation](https://docs.oracle.com/javase/8/docs/api/java/lang/StringBuilder.html)

We have just seen that strings are collection of characters that, once created, cannot be modified. 
But now we will see just the opposite, how to create strings that can be modified, and that thanks to **StringBuilder**, as `StringBuilder` provide
a dynamic capacity.

#### Important considerations
It is very important to know that Java can do some optimizations that involve `String` objects instances, like make references to 
a `String` object from multiples variables, because Java knows that `String`s are immutables and its value won't change. So if the state of the 
string won't change please use `String` object and don't use `StringBuilder`.

If you are tasked to write a program that will work with `String`s and a lot of manipulations over those `String`s will happen, please use 
`StringBuilder` because it is more efficient do those operations over a `StringBuilder`.

Another important fact is that objects of `StringBuilder` are not secure to use them with `Thread` (a concept we will see soon). If you have
the case that multiples `Threads` please use `StringBuffer`, both `StringBuilder` and `StringBuffer` offer dynamic capacity, but `StringBuffer`
is more secure with `Threads`.

We will be working with `Threads` sooner. Don't worry about it, is a concept that is very important but for now does not matter now.

#### How to create Strings with StringBuilder

StringBuilder set the capacity of the instance base on the passed string length + 16.

```java
StringBuilder str = new StringBuilder();
System.out.println(str.capacity()); // Output: 16
System.out.println(str.length()); // Output: 0
```

Now let's see another case:

```java
StringBuilder str = new StringBuilder("Hello");
int len = str.length();
System.out.println(len == 5); // Output: true
System.out.println(str.capacity() == len + 16); // Output: true
```

As you can see we made some type of asserting using the `StringBuffer#length`, wich return the total characters in the instance, and
we proved that the capacity is equal to the total of the current characters + 16.


#### The following operations you can apply to `StringBuilder`
- Insert at any position
- Delete any character, substring, etc
- Reverse
- Replace
- Substrings
- etc