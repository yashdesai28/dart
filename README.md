
# Project Title

A brief description of what this project does and who it's for


# Flutter


The main entry point

Every application has some point in its program that serves as the entry point to the application. When an application runs, it starts from that specified entry point. In Dart, the entry point is the main() function. You might be unfamiliar with what a function is at this point; that’s okay. For now, just remember that when you run a Dart program, the compiler looks for the main() function and executes the code written in that function. If main() is not found, you will get an error and your application won’t run. The code you write in main() is encapsulated in curly brackets ({}). Let’s look at the general syntax below.


```
main() {
  // Printing the text 'Hello World'
  print("Hello World");
}

```
Nothing without a semicolon

Comments
```
// Insert comment here
```
Imperative programming

The code that appears inside of the main() function gets executed in order of appearance. Let’s modify the code in the snippet above and try printing From Dart along with Hello World.

```
main() {
  print("From Dart");
  print("Hello World");
  
}
```

Overview
Understanding the Code
Libraries
Taking Input in Dart

```
import 'dart:io';

main() {
    print("Hello " + stdin.readLineSync());
}
```

On line 1 of the code above, we are importing the dart:io library. In computer programming, a library is a collection of similar code that you can reference in your own code. When you import a library, you can access all the code in that library.

Every library has a particular purpose. 
# The dart:io library provides I/O (Input/Output)
 support for non-web applications. We imported dart:io because the program we wrote requires input from the user.

# Taking Input in Dart
Dart provides multiple methods that can be used to take external input from a user depending on the type of input required by the program. For this course, we will be using the readLineSync() method (function) which reads a line from the input.

The complete expression we will use is stdin.readLineSync(). stdin stands for standard input, letting the compiler know that the program specifically requires some sort of input from the user. readLineSync() is a built-in method that we have already discussed above.

Line 4 is displaying Hello and then concatenating (joining) it with the input provided by the user using the addition (+) operator (a topic we will discuss later in the course).

That’s pretty much all there is to the code written above.


# Objects in reality
Objects are all around us. From the food we eat to the pets we own, everything is an object.

Every object has characteristics and behaviors. For instance, a person has characteristics such as their name, age, and height. A person can also perform behaviors such as walking, eating, and sleeping. These characteristics and behaviors combined define who the person is.


Objects in Dart
In the same way, everything in Dart is an object. Objects in a programming language also have characteristics known as properties and they can also perform behaviors known as methods. Properties represent what the object knows, and methods represent what the object can do.


# Dart’s built-in data types
The Dart language has special support for the following types:

Numbers
Strings
Booleans
Lists
Sets
Maps
Runes
Symbols

```
main() {
  String country = "Japan";

  print("I want to visit $country");
}
```

The $ sign can also be followed by an expression delimited by curly brackets.

```
main() {
  print("The sum of 5 and 3 equals ${5+3}.");
}
```
{expression}

In the code above, 5+3 is our expression which the compiler processes and interprets to 8, as can be seen in the output when you press RUN.

Multiple lines
You can concatenate strings using adjacent string literals as well.

```
main() {
  var s1 = 'String '
    'concatenation'
    " works even over line breaks.";
    
  print(s1);
}
```

```
main() {
  var multilineString = """This is a 
multiline string
consisting of 
multiple lines""";

  print(multilineString);
}
```

out put 

This is a 
multiline string
consisting of 
multiple lines

```
main() {
  bool greater;
  greater=5>3;
  print(greater);
}
```
Type inference allows us to declare a variable without explicitly mentioning the data type. In Dart, we insert the var keyword in place of the data type.

```
main() {
  var bookTitle = "Lord of the Rings: The Fellowship of the Ring";
  var bookAuthor = "J. R. R. Tolkien";
  var bookNoOfPages = 423;

  // Driving Code
  print(bookTitle);
  print(bookAuthor);
  print(bookNoOfPages);
}
```

Checking the type

Remember when we said objects have properties which represent the information the object knows? Well, runtimeType is one such property that holds information about the data type of the variable.

In the code snippet below, we are printing the data type of the variable bookTitle by calling its property runtimeType.

```
main() {
  var bookTitle = "Lord of the Rings: The Fellowship of the Ring";

  print(bookTitle.runtimeType);
}
```
Output

String

Dynamic types
If you want a variable to hold objects of many types, you can declare a variable using the dynamic keyword.

main() {
  dynamic dynamicVariable = 'A string'; // type String
  print(dynamicVariable);

  dynamicVariable = 5; // type int
  print(dynamicVariable);

  dynamicVariable = true; // type bool
  print(dynamicVariable);
}

++var	var = var + 1
var++	var = var + 1
--var	var = var - 1
var--	var = var - 1

# The ++ var expression

The expression value of ++var is var+1. When we insert the expression in a print statement, the compiler first increments the variable by 1 and then prints the value of the variable.

```
main() {
  var prefixIncrement = 5;

  print(++prefixIncrement);
}
```

Output

6

# The var ++

The expression value of var++ is var. When we insert the expression in a print statement, the compiler first prints the value of the variable and then increments it by 1.

```
main() {
  var postfixIncrement = 5;

  print(postfixIncrement++);
  print(postfixIncrement);
}
```

Output

5
6

# The -- var expression
The expression value of --var is var-1. When we insert the expression in a print statement, the compiler first decrements the variable by 1 and then prints the value of the variable.

```
main() {
  var prefixDecrement = 5;

  print(--prefixDecrement);
}
```

Output

4

# The var -- expression
The expression value of var-- is var. When we insert the expression in a print statement, the compiler first prints the value of the variable and then decrements it by 1.

Output

5
4

# Type Test Operators
as	typecast
is	True if the object has the specified type
is!	False if the object has the specified type

```
main() {
  double type1 = 5.0;
  int type2 = 87;
  String type3 = "educative";
  bool type4 = true;

  print(type1 is int);
  print(type2 is int);
  print(type3 is String);
  print(type4 is double);
  print(type4 is! double);
}
```

Output

false
true
true
false
true


# Adding a single element

```
main() {
  var listOfVegetables = ['potato', 'carrot', 'cucumber'];

  listOfVegetables.add('cabbage');

  print(listOfVegetables);
}
```

# Adding multiple elements

```
// First method
listName.addAll([elem 1, elem 2, ..., elem n])
// Second method
listName.addAll(otherListName)
```

```
main() {
  var listOfVegetables = ['potato', 'carrot', 'cucumber', 'cabbage'];

  listOfVegetables.addAll(['broccoli', 'zucchini']); 

  print(listOfVegetables);

  var vegetablesToAdd = ['okra', 'capsicum'];

  listOfVegetables.addAll(vegetablesToAdd);

  print(listOfVegetables);
}
```

Output

[potato, carrot, cucumber, cabbage, broccoli, zucchini]
[potato, carrot, cucumber, cabbage, broccoli, zucchini, okra, capsicum]

# Removing a single element

```
main() {
  var listOfVegetables = ['potato', 'carrot', 'cucumber', 'cabbage', 'broccoli', 'zucchini'];

  listOfVegetables.removeAt(0);
  print(listOfVegetables);

  listOfVegetables.removeAt(2);
  print(listOfVegetables);
}
```

Output

[carrot, cucumber, cabbage, broccoli, zucchini]

[carrot, cucumber, broccoli, zucchini]

# Removing all elements

```
main() {
  var listOfVegetables = ['cucumber', 'zucchini'];

  listOfVegetables.clear();

  print(listOfVegetables);
}
```

# The map() Method

```
main() {
  var integers = [1,2,3];
  var cubes = integers.map((integer) => integer * integer * integer).toList();
  print(cubes);
}
```

# Creating a set
```
main() {
  var simpleSet = {1,2,3};

  print(simpleSet);
}
```
