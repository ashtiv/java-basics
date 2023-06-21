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
