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
# Constructors in Java

Constructors are special methods that initialize an object when it is created.

## Constructor Part 1

-   Constructors have the same name as the class
-   Constructors are used to initialize object's state when it is created
-   A  default constructor  is provided if no constructor is defined

```
class Phone {
  
  String brand;
  
  Phone(){  
    // default constructor
  }
  
  Phone(String brand){
    this.brand = brand; 
  }
}

```

We can call the constructors when creating objects:

```
Phone p1 = new Phone();
Phone p2 = new Phone("Apple");

```

## Constructor Part 2

-   Multiple constructors can be defined with different parameters
-   Constructors can call other constructors using  `this()`
-   This is called  constructor chaining

```
class Phone{
  
  String brand;
  String model;
  
  Phone(String brand){
    this.brand = brand;  
  }
  
  Phone(String brand, String model){
    this(brand);
    this.model = model; 
  }
}

```

Here the second constructor calls  `this(brand)`  to call the first constructor, then initializes the  `model`  field.

-   We must call  `this()`  as the first statement if chaining constructors
-   It delegates the  object initialization  to another constructor.

# Reference vs Object vs Instance vs Class

## Reference

-   A reference is a variable that holds the memory location of an object
-   It does not contain the actual object, but refers to the memory location where the object is stored
-   References are created when a new object is instantiated

```
Phone samsung = new Phone(); // samsung is a reference

```

Here  `samsung`  is a reference that refers to the memory location of the newly created  `Phone`  object.

## Object

-   An object is an instance of a class, with state and behavior
-   It has identity, state and behavior
-   An object is a  runtime entity  that occupies space in memory

```
Phone samsung = new Phone();

```

Here a  `Phone`  object is created and  `samsung`  refers to it.

## Instance

-   An instance is a specific object created from a  class blueprint
-   A class is like a blueprint and an instance is a concrete object created based on that blueprint.


```
Phone samsung = new Phone(); 
Phone apple = new Phone();

```

Here  `samsung`  and  `apple`  are two instances of the  `Phone`  class.

## Class

-   A class defines the state and behavior that objects of that class will have
-   It is a template/blueprint that describes the nature of objects that can be created from it.

```
class Phone {
   ...
}

```

Here  `Phone`  is a class that defines the state and behavior for  `Phone`  objects.

So in summary:

-   A reference refers to an object
-   An object is an instance of a class
-   An instance is a specific object created from a class
-   A class defines the blueprint for objects.

# Static vs Instance

## Instance Variables

-   Belong to objects (instances of a class)
-   Each object has a separate copy of  instance variables
-   Accessed using  object reference  (instance)
-   Life cycle  - exist as long as the object exists
-   Examples:
    -   name
    -   age
    -   salary
-   Declared as:

```
class Employee {
  String name;  // instance variable
  int age;
}

```

## Static Variables

-   Belong to the class
-   Shared among all objects of that class
-   Accessed using  class name, not a particular object
-   Life cycle - exist as long as class is loaded
-   Examples:
    -   numberOfEmployees
    -   taxRate
-   Declared as:

```
class Employee {
  static int numberOfEmployees;  // static variable  
}

```

## Instance Methods

-   Operate on instance variables
-   Accessed using object reference
-   Can access instance variables and other  instance methods
-   Cannot access  static variables/methods directly
-   Examples:
    -   getSalary()
    -   hireDate()
-   Declared as:

```
public void getSalary() {
  // use instance variables
}

```

## Static Methods

-   Accessed using class name
-   Operate on static variables
-   Can access static variables/methods
-   Can access instance variables/methods using object reference
-   Examples:
    -   calculateSalary()
    -   getTaxRate()
-   Declared as:

```
public static int calculateSalary() {
  // use static variables  
}

```

So in summary:

-   Instance variables/methods belong to objects and deal with object state
-   Static variables/methods belong to the class and deal with class state
-   Static  variables/methods exist independently of any object.

# POJOs and Records in Java

## POJOs

-   POJO stands for  Plain Old Java Object
    
-   It is a Java object that does not extend any class other than Object
    
-   It has no dependencies on specific classes
    
-   POJOs have:
    
    -   Fields (properties)
    -   Getters and setters for the fields
    -   A no-arg constructor
-   They are simple, lightweight objects used to transfer data.
    

Example:

```
public class User {
  
  private int id;
  private String name;  
  
  // getters and setters
  // no-arg constructor
}

```

POJOs are commonly used:

-   As form backings in  web applications
-   For transferring data to/from databases
-   For serialization

## Records

-   Records are a new Java language feature added in  Java 14
-   Records are POJOs with some additional functionality:
    -   Component-based access
    -   Sensible  `toString()`,  `equals()`  and  `hashCode()`
    -   A transparent constructor

Example:


```
public record User(int id, String name) {}

```

-   This creates:
    -   Fields  `id`  and  `name`
    -   A constructor  `User(int id, String name)`
    -   `toString()`,  `equals()`  and  `hashCode()`  methods
    -   Accessors for the fields using  `User.this.id`  and  `User.this.name`

We can create a record like:


```
User user = new User(1, "John");

```

And access fields using:

```
int id = user.id();

```

-   Records are immutable by default, fields cannot be reassigned
-   We can make records mutable using  `with()`

# Annotations in Java

Annotations are metadata that provide data about the code. They do not modify the code itself.

Annotations have a  `@`  sign followed by an annotation name:

```
@Override
@SuppressWarnings("unchecked")

```

Some common uses of annotations are:

-   Compiler  checks -  `@Override`,  `@Deprecated`
-   Frameworks -  `@Autowired`,  `@Entity`
-   Documentation  -  `@param`,  `@return`

## Declaring Annotations

Annotations are declared using the  `@interface`  keyword:

```
@interface MyAnnotation {
  // Attributes
}

```

Attributes can be:

-   Primitive types -  `int`,  `float`,  `boolean`
-   Strings
-   Enumerations
-   Annotations
-   Arrays of the above
-   Class literals

Example:


```
@interface Author {
  String name(); 
  int age() default 30;
}

```

Here we have a  `String`  attribute  `name`  and an  `int`  attribute  `age`  with a default value.

## Using Annotations

We annotate classes, methods, fields:


```
@Author(name = "John")
public class MyClass {
    
  @Author  
  public void doSomething() {
      
  }
}

```

We can retrieve annotations at runtime using reflection:


```
Author author = MyClass.class.getAnnotation(Author.class);
String name = author.name();

```

## Built-in Annotations

Java has some annotations built-in:

-   `@Override`  - Checks that a method overrides its superclass
-   `@Deprecated`  - Marks a method/class as deprecated
-   `@SuppressWarnings`  - Suppresses compiler warnings

## Retention Policy

Annotations can have 3 retention policies:

-   `SOURCE`  - Discarded after compilation
-   `CLASS`  - Retained after compilation, available to classloader (default)
-   `RUNTIME`  - Available at runtime through reflection

We set the retention using  `@Retention`:

```
@Retention(RetentionPolicy.RUNTIME)
public @interface MyAnnotation {
  ...   
}
```
# Inheritance - Part 1

Inheritance  allows us to define a class (called subclass) that inherits the properties and behaviours of another class (called  super class  or  parent class).

The subclass inherits the:

-   variables
-   methods
-   constructors  
    from the superclass.

The subclass can:

-   add its own fields and methods in addition to the inherited ones.
-   override the methods of the superclass.

```
class Superclass {
    // variables, methods and constructors 
}

class Subclass extends Superclass {
    // inherits variables, methods and constructors from Superclass 
    // can add its own fields and methods  
    // can override methods 
}

```

# Inheritance - Part 2

The  `extends`  keyword indicates that the subclass inherits from the superclass.

In Java, a subclass can only inherit from a single superclass but the superclass can have multiple subclasses.

Constructors are not inherited but the subclass constructor calls the  superclass constructor  using  `super()`.

```
class Animal {
  
}

class Dog extends Animal {
   
}

class Cat extends Animal {
   
}

```

# Inheritance - Part 3

The subclass inherits the:

-   private variables and methods of the superclass.
-   But the subclass cannot directly access private members of the superclass.

The subclass can access:

-   protected
-   public  
    members of the superclass.

# What is  java.lang.Object?

java.lang.Object is the ultimate superclass for all classes in Java.

Even if a class does not explicitly extend any class, it implicitly extends  `java.lang.Object`.
For example:

```
class Dog {
    
}
// Inherits from Object implicitly
class Dog extends Object { 
    
}

```

The  `java.lang.Object`  class defines the most generic methods like:

-   `equals()`  - compares two objects
-   `hashCode()`  - returns the  hash code value  of an object
-   `toString()`  - returns a string representation of an object
-   `getClass()`  - returns the Class object
-   `clone()`  - creates a clone of an object
-   `finalize()`  - called by the  garbage collector  before an object is garbage collected

All classes in Java inherit these methods from Object

# Inheritance Challenge - Part 1

Demonstrates defining subclasses and using inheritance in a simple sample program.

# Inheritance Challenge Part 2

Extends the previous inheritance example with additional logic and method overriding.

# this vs super

In the subclass, use  `super()`  to call the superclass constructor.

Use  `super.method()`  to access the  superclass method  overridden in the subclass.

Use  `this.member`  to access the  subclass fields  and methods.

```
class Animal {
    String name;
    
    public Animal(String name) {
        this.name = name;
    }
}

class Dog extends Animal {
    
    public Dog(String name) {
        super(name);  // Calls Animal constructor
    }
    
    public void printName() {
        System.out.println(this.name); // Accesses Dog's name field
        System.out.println(super.name); // Accesses Animal's name field
    }
}

Dog dog = new Dog("Tommy");
dog.printName();

```

Output:


```
Tommy  
Tommy

```

`this`  refers to the current object i.e. Dog instance.

`super`  refers to the  super class  i.e. Animal. It allows the subclass to invoke the  superclass methods  and fields.

# Method Overloading vs  Overriding  Recap

## Method  Overloading

Method overloading  is defining multiple methods with the same name but different parameters  **within the same class**.

### Example

```
class Add{  
  void add(int a, int b){
    System.out.print(a+b);  
   }    
  void add(int a, int b, int c){  
    System.out.print(a+b+c);
  }
}

```

Here we have two  `add()`  methods with different number of parameters. This is method overloading.

Characteristics of Method Overloading:

-   Same method name
-   Different parameters
-   Within same class
-   Compile time polymorphism

## Method Overriding

Method overriding  is defining a method in the  child class  with the same name and arguments as in the parent class.

### Example

```
class Animal{  
  void eat(){
    System.out.print("Animal is eating");
  }
}

class Dog extends Animal{
  void eat(){ 
    System.out.print("Dog is eating"); 
  }
}

```

Here we have an  `eat()`  method in the parent  `Animal`  class and then we override it in the child  `Dog`  class.

Characteristics of Method Overriding:

-   Same method name and parameters
-   Different implementation
-   In child and parent classes
-   Run time polymorphism
