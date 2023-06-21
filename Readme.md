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
    

Hope this helps! Let me know if you have any other questions.
