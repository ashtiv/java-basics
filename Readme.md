# Expressions and Keywords in Java

## Keywords

Keywords are  reserved words  in Java that have special meaning to the compiler. Some keywords:

-   `class`
-   `public`
-   `private`
-   `protected`
-   `void`
-   `if`
-   `else`
-   `for`
-   `while`
-   `switch`
-   `return`
-   `break`
-   `continue`

Keywords cannot be used as identifiers (variable names,  class names, etc).

## Expressions

An expression is a combination of operands and operators that evaluate to a value.

Some examples of expressions:

-   Arithmetic  expressions:


```
int a = 5 + 6;
int b = a * 2; 

```

-   Relational expressions:


```
a > b
a <= b

```

-   Logical expressions:


```
a && b
a || b 

```

-   Assignment expressions:


```
a = b;
c += 5; 

```

-   Variable reference expressions:


```
String name;
name = "John";

```

-   Increment/decrement expressions:


```
a++;
b--;

```

-   Method call expressions:


```
max(a, b) 

```

## Variable Declaration

Variables are declared in Java using:

-   Primitive data types:  `int`,  `double`,  `char`,  `boolean`
-   Reference data types:  `Class`  names

Syntax:

`dataType variableName;`

Example:

`int number;`  
`String name;`

That covers the basics of keywords and expressions in Java! Let me know if you have any other questions.

# Statements, Whitespace and Indentation in Java

## Statements

A statement in Java performs some action and potentially changes the state of the program. Some examples of statements in Java:

-   Variable declarations:

```
int number;
String name;

```

-   Assignment statements:

```
number = 10;
name = "John";

```

-   Method invocation statements:


```
printMessage();

```

-   if-else statements:


```
if (number > 0){
    //...
} else {
    //..
}

```

-   while loops:


```
while(number < 100){
    number++;  
}

```

-   for loops:


```
for(int i = 0; i < 10; i++){
    //...
}

```

-   return statements:


```
return number; 

```

-   throw statements:


```
throw new Exception("Error!");

```

## Whitespace and Indentation

Java is sensitive to whitespace and indentation:

-   Whitespace includes spaces, tabs and  line breaks.
    
-   Java uses whitespace to determine where a statement begins and ends.
    
-   Indentation is not technically required in Java, but it is considered good practice to make the code more readable.
    
-   The  Java compiler  ignores whitespace, except:
    
-   Inside string literals:
    


```
String s = "This has   spaces"; 

```

-   As separators between tokens:

```
int a = b;  //Semicolon required

```

So while whitespace and indentation do not affect the functioning of Java code, they improve readability and maintainability.  Consistent indentation  (e.g. using 4 spaces) is recommended.

## Best Practices

Some best practices regarding statements, whitespace and indentation in Java:

-   Use whitespace and newlines to visually group related lines of code
    
-   Indent after opening { and outdent before closing }
    
-   Place each statement on a new line
    


```
int a = 1;  
int b = 2;
int c =  a + b;

```

-   Limit line length  to around 80 characters
    
-   Be consistent with your indentation (e.g. 4 spaces)
    

# Code Blocks And The If Then Else Control Statement in Java

In this article we will discuss:

-   Code blocks  in Java
-   The if-then-else control statement
-   Syntax and examples

## Code Blocks

A code block in Java is a group of zero or more statements between opening  `{`  and closing  `}`  brackets.

-   Code blocks can be used anywhere a single statement is expected.
-   Code blocks allow grouping multiple statements into a single statement.

For example, the  `if-then-else`  statement requires a code block for its  `then`  and  `else`  parts:


```
if (condition) {
    // code block - then part 
    statement1;
    statement2; 
} else {
    // code block - else part
    statement3;
    statement4;
}

```

Code blocks are also used with  `for`,  `while`,  `do-while`,  `switch`  statements, method definitions, etc.

## If-Then-Else Statement

The  `if-then-else`  statement is Java's conditional statement. It has the following syntax:


```
if (condition) {
    // code block - then part
} else {
    // code block - else part 
}

```

The condition is evaluated, and if it evaluates to  `true`, the then part is executed. Otherwise the else part is executed.

Example:


```
int number = 5;

if (number % 2 == 0) {
    System.out.println("Number is even.");
} else {    
    System.out.println("Number is odd.");  
}
// Prints "Number is odd."

```

You can use an  `if`  statement alone, without the  `else`  part.

You can also nest  `if-else`  statements:

```
if (condition1) {
    ...
} else if (condition2){
    ...
} else {
    ...
}  
```

# Methods in Java

Methods are functions that contain reusable blocks of code to perform a specific task.

## Defining a Method

To define a method in Java, we use the  `public`  and  `static`  access modifiers, followed by the  `return type`  of the method, the  `method name()`  and the list of  `parameters`  inside parentheses.

The basic syntax is:

```
access-modifier return-type method-name(parameter-list){
   // method body
}  

```

For example:

```
public static int sum(int a, int b){
    int total = a + b;
    return total;
}

```

Here:

-   `public`  - Access modifier
-   `static`  - Method can be accessed without creating an object
-   `int`  - Return type
-   `sum()`  - Method name
-   `(int a, int b)`  - Parameters
-   `{...}`  - Method body

## Invoking a Method

To invoke or call a method, use the  method name  and pass the arguments:

```
int result = sum(5, 10);  // Call the sum() method and pass 5 and 10 

```

## Method Parameters

-   Parameters act as variables that store the values passed to the method.
-   Parameters are specified inside the parentheses () after the method name.
-   Parameters can be primitive types or reference types.
-   Parameters are method-local; they exist only during the method call.

## Return Type

-   The  return type  specifies the data type returned by the method.
-   `void`  is used for methods that do not return any value.
-   We use the  `return`  statement to return a value from a non-void method.

For example:


```
public static int sum(int a, int b){
    int total = a + b;
    return total;   // Return the sum  
}
```

# Method Overloading in Java

Method overloading is an important feature of  Object Oriented Programming  in Java. It allows us to define multiple methods with the  **same name but different parameters**.

When a method is called, Java perform  overload resolution  using the number, type and order of parameters to determine the best  matching method.

## Rules for Method Overloading:

-   Method overloading is  _possible_  only when method has  _different parameters_.
-   Method overloading is  _not possible_  by changing return type.
-   Method overloading is  _possible_  by changing number of parameters.
-   Method overloading is  _possible_  by changing type of parameters.
-   Method overloading is  _possible_  by changing order of parameters.

## Example:

```
class MethodOverloading{  
    void add(int a, int b){
        System.out.println(a + b);
    }  
    void add(int a, int b, int c){   
        System.out.println(a + b + c);
    }  
    void add(double a, double b){  
        System.out.println(a + b);
    }  
}

```

Here  `add()`  method is overloaded based on:

-   Number of parameters
-   Type of parameters

## Benefits of Method Overloading:

-   Provides reusability of method name.
-   Makes code easy to read and understand.

# The switch statement

The  `switch`  statement in Java allows us to select one of many code blocks to execute. It provides an alternative to multiple  `if-else if`  statements.

The basic syntax is:

```
switch (expression) {
   case x: 
      // code block  
      break; 
   case y:
      // code block
      break;  
   default:
      // code block
}

```

We can make efficient  switch statements  by:

-   Using the  `break`keyword only at the end of the last  `case`:


```
switch(expression) {
  case 1:  
  case 2: ->  
     // code
     break;    
  case 3:  
     // code 
     break;    
}

```

-   Omitting the  `default`  case if not needed.

String values can also be used:


```
String day = "Monday";

switch (day) {
  case "Monday": ->
     // code  
     break;   
  case "Friday": ->
     // code  
     break;    
}

```

Example:
```
int number = 3;

switch(number) {
  case 1:  
  case 2: ->  
     System.out.println("Number is 1 or 2");       
  case 3: ->
     System.out.println("Number is 3");  
}  
// Number is 1 or 2     
// Number is 3

```

The  `->`  arrow notation  visually represents the fall-through from one case to the next.

# Loops in Java

Loops allow us to execute a block of code repeatedly based on a condition.

## While  Loop

The  `while`  loop executes a block of statements as long as a condition is true:


```
while (condition) {
   // code block to be executed
}

```

Example:

```
int i = 1;
while (i <= 5) {
    System.out.println(i);
    i++; 
}
// Prints 1 2 3 4 5

```

## Do-While Loop

The  `do-while`  loop is similar but executes the block at least once, then checks the condition:

java

Copy

```
do {
   // code block to be executed
} while (condition);

```

Example:


```
int i = 6;
do {
   System.out.println(i);
   i++;
} while (i <= 5);
// Prints 6

```

## For Loop

The  `for`  loop has the following structure:

```
for (initialization; condition; increment) {
    // code block to be executed
}

```

-   `initialization`  happens once, before the loop
-   `condition`  is checked each time before executing the block
-   `increment`  is executed at the end of each loop

Example:

```
for (int i = 1; i <= 5; i++) {
   System.out.println(i);
}
// Prints 1 2 3 4 5

```

For loops are often used to iterate over arrays:


```
for (int i = 0; i < arr.length; i++) {
   System.out.println(arr[i]); 
}
```
# Local Variables and Scope in Java

A variable declared within a method or block is called a local variable.

The scope of a  local variable  is the region of the program where it can be referenced.

For example:


```
class Test {
   public void method1() {
      int number = 10;  
      // number is local to method1()
   }
   
   public void method2() {
      int number = 20;    
      // number is local to method2()
   }  
}

```

Here,  `number`  is a local variable with scope within the method it is defined.

It cannot be accessed outside of that method.

## Block Scope

A variable declared within a block  `{ }`  has  block scope  and is only accessible within that block:

```
void method() { 
    int number = 10;
    
    if(number > 5) {
        int result = number * 2;   
        // result has block scope 
    }
    
    // result cannot be accessed here
}

```

## Shadowing

When a local variable has the same name as a variable in an outer scope, it shadows the outer variable.

The inner variable then takes precedence:

```
int number = 10;

void method() {
   int number = 20; 
   System.out.println(number); // Prints 20
}

System.out.println(number); // Prints 10

```

Here, the  `number`  variable within  `method()`  shadows the outer  `number`  variable.

## Lifetime

A local variable exists from the time its declared until the closing  `}`  of the method or  block.  
After that, it ceases to exist.

# Parsing Values and Reading Input using System.console()

The  `System.console()`  method allows us to read input from the console in Java. It returns a  `Console`  object which has various methods to read input.

## Reading String Input

We can read a String input using the  `reader()`  method of the  `Console`  object:
```
Console console = System.console();

String name = console.reader().readLine();

```

This will read a line of input from the console and store it in the  `name`  variable.

## Reading Integer Input

We can read an  `int`  input using the  `readInt()`  method:

```
Console console = System.console();

int age = console.readInt();

```

This will read an integer from the console and store it in the  `age`  variable.

It will throw an  `InputMismatchException`  if the input is not a valid integer.

## Reading other types

Similar methods exist to read  `long`,  `float`,  `double`,  `char`  etc. For example:
```
long no = console.readLong();
float price = console.readFloat();
char letter = console.readChar();

```

## Hiding Input

To read a password or other  sensitive input, we can use the  `readPassword()`  method:

```
char[] password = console.readPassword();
String passStr = String.valueOf(password);

```

This will read the input and hide it on the console, storing it in a  character array.

# Exception Handling with System.console()

When reading input using  `System.console()`, exceptions can be thrown if the input is invalid.

We can catch and handle these exceptions using a  `try-catch`  block:

```
try {
    int age = console.readInt(); 
} catch(InputMismatchException e) {
    // Handle exception    
}

```

This will catch if the user enters non-integer input and then we can handle the exception accordingly.

We can also use the  `finally`  block to execute code regardless of whether an exception was thrown or not:
```
try {
    // read input  
} catch (Exception e) {
  
} finally {
    // cleanup resources
}

```

# Introduction to Scanner

The  `Scanner`  class is another useful tool for reading  console input  in  Java.

We can create a  `Scanner`  object from  `System.in`  which represents the standard input:

```
Scanner sc = new Scanner(System.in);

```

Then we can use various methods to read different types of input:

-   `nextInt()`: Read integer
-   `nextDouble()`: Read double
-   `nextFloat()`: Read float
-   `nextLine()`: Read entire line of input as String
-   `next()`: Read next token (separated by whitespace)

For example:

```
int a = sc.nextInt();
double b = sc.nextDouble(); 
String name = sc.nextLine();

```

The  `Scanner`  class also throws exceptions which we can catch in a  `try-catch`  block.

# Reading Input  with Scanner

As mentioned earlier, we can use the Scanner class to read user input from the console.

Some key methods for reading input are:

-   `nextLine()`: Reads the entire line of input and returns a String.

```
Scanner sc = new Scanner(System.in);
String name = sc.nextLine();

```

-   `next()`: Reads the next token (separated by whitespace) and returns a String.

```
String word = sc.next();

```

-   `nextInt()`: Reads an int.

```
int age = sc.nextInt();

```

-   `nextDouble()`: Reads a double.

```
double gpa = sc.nextDouble();

```

-   `nextBoolean()`: Reads a boolean.


```
boolean isCorrect= sc.nextBoolean();

```

We can catch exceptions thrown by Scanner using a try-catch block:


```
try {    
    int num = sc.nextInt(); 
} catch (InputMismatchException e) {
    // Handle exception  
}

```

It is good practice to close the Scanner after use:


```
sc.close();

```

This releases the resources used by the Scanner. We can do this in a finally block:


```
try {
    // read input 
} finally {
    sc.close(); 
}
```
# Classes and Objects in  Java

## Introduction to Classes and Objects

Classes allow us to model  real world objects, like  `Car`  or  `Phone`

An object is an instance of a class, with its own properties and methods  
A class defines the blueprint and objects are instances of that blueprint

To define a class in Java:

```
class ClassName {
   // variables 
   // methods   
}

```

Variables in a class are called fields (aka properties, attributes)  
Methods define the behaviors of the object

## Using  Getter  Methods

Getter methods allow us to retrieve an object's field values  
Getter methods have "get" in the name and return the field value

```
class Phone {
   private string brand;

   public string getBrand() {
       return brand;
   }
}

```

## Using Setters

Setter methods allow us to update an object's field values  
Setter methods have "set" in the name and take a parameter
```
class Phone {
    private string brand;
    
    public void setBrand(string newBrand) {
        brand = newBrand;   
    }
}

```

## Creating Objects

We create objects using the  `new`  keyword and the class name:


```
Phone myPhone = new Phone();

```

We can then call methods and access fields of that object:


```
myPhone.setBrand("Samsung");
String brand = myPhone.getBrand();

```
