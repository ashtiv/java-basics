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

Copy

```
int a = 5 + 6;
int b = a * 2; 

```

-   Relational expressions:

Copy

```
a > b
a <= b

```

-   Logical expressions:

Copy

```
a && b
a || b 

```

-   Assignment expressions:

Copy

```
a = b;
c += 5; 

```

-   Variable reference expressions:

Copy

```
String name;
name = "John";

```

-   Increment/decrement expressions:

Copy

```
a++;
b--;

```

-   Method call expressions:

Copy

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

java

Copy

```
int number;
String name;

```

-   Assignment statements:

java

Copy

```
number = 10;
name = "John";

```

-   Method invocation statements:

java

Copy

```
printMessage();

```

-   if-else statements:

java

Copy

```
if (number > 0){
    //...
} else {
    //..
}

```

-   while loops:

java

Copy

```
while(number < 100){
    number++;  
}

```

-   for loops:

java

Copy

```
for(int i = 0; i < 10; i++){
    //...
}

```

-   return statements:

java

Copy

```
return number; 

```

-   throw statements:

java

Copy

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
    

java

Copy

```
String s = "This has   spaces"; 

```

-   As separators between tokens:

java

Copy

```
int a = b;  //Semicolon required

```

So while whitespace and indentation do not affect the functioning of Java code, they improve readability and maintainability.  Consistent indentation  (e.g. using 4 spaces) is recommended.

## Best Practices

Some best practices regarding statements, whitespace and indentation in Java:

-   Use whitespace and newlines to visually group related lines of code
    
-   Indent after opening { and outdent before closing }
    
-   Place each statement on a new line
    

java

Copy

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

java

Copy

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

java

Copy

```
if (condition) {
    // code block - then part
} else {
    // code block - else part 
}

```

The condition is evaluated, and if it evaluates to  `true`, the then part is executed. Otherwise the else part is executed.

Example:

java

Copy

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

java

Copy

```
if (condition1) {
    ...
} else if (condition2){
    ...
} else {
    ...
}  
```
