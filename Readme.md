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

![Screenshot from 2023-06-22 09-50-33](https://github.com/ashtiv/java-basics/assets/75435020/34903314-93da-4422-9edd-b921bcde303b)

# The Text Block and other  Formatting Options  in  Java

## Text Blocks

Java 16  introduces  text blocks, which make multi-line strings easier to read and write. A  text block  is defined using `""":

```
String text = """
This is a 
 multi-line 
 string""";

```

The three double quotes indicate that the following string can span multiple lines. The string retains the whitespace,  line breaks  and format.

You can interpolate variables into a text block:

```
String name = "John";
String greeting = """
Hello 
  $name!"""; 
// greeting is "Hello  
   John!"

```

The  `$`  indicates a variable to interpolate.

Compare text blocks to concatenation:

```
String multiLine =  
"Hello " +  
"World!";

String multiLine = """
Hello  
  World!""";

```

Text blocks are much more readable.

## String Formatting

-   String padding - Add spaces to make a string a certain length:

```
String s = String.format("%10s", "Hi");
// s is "Hi         " 

```

Use  `-`  for left align,  `^`  for center and  `>`  for right align.

-   Number formatting - Use format specifiers:

```
String.format("%d", 100);  // 100  
String.format("%.2f", 1.23); // 1.23

```

-   Escaping - Use  `\`  to escape characters:

```
System.out.println("Hello\nWorld!");
// Prints:
// Hello  
// World!

```

-   String alignment:

```
String.format("%-10s", "Hi"); // "Hi        "  
String.format("%10s", "Hi"); //"        Hi"
String.format("%^10s", "Hi"); // "   Hi     "
```
# Another Look at the String

Strings are immutable in Java, meaning they can't be changed once created. This leads to inefficiencies when performing string manipulations.

Some string methods:

-   `length()`  - Returns the length of the string
-   `charAt()`  - Returns the character at the specified index
-   `concat()`  - Concatenates two strings
-   `compareTo()`  - Compares two strings lexicographically
-   `startsWith()`/`endsWith()`  - Checks if string starts/ends with specified string
-   `substring()`  - Extracts a substring from the specified indices
-   `replace()`  - Replaces occurrences of one string with another
-   `trim()`  - Removes whitespace from both ends of a string

String objects are pooled - if two strings have the same value, they will point to the same object. This pooling helps save memory.

## String Manipulation Methods

Common string manipulation methods:

-   `toLowerCase()`/`toUpperCase()`  - Converts string to lower/upper case
-   `strip()`  - Removes leading/trailing whitespace
-   `trim()`  - Removes leading and trailing whitespace
-   `replace()`  - Replaces occurrences of a substring
-   `split()`  - Splits a string into an array using a delimiter
-   `join()`  - Joins an array of strings into one string using a delimiter

Examples:
```
String s = " Hello World ";
s = s.strip(); // "Hello World"
s = s.trim(); // "Hello World"
s = s.replace("e", "a"); // "Hallo World"
String[] parts = s.split(" ");  
String newString = String.join("-", parts);
// newString is "Hallo-World"

```

## The StringBuilder class

`StringBuilder`  is a mutable sequence of characters.  
Since strings are immutable, concatenating strings creates new objects.  
`StringBuilder`  avoids this overhead, making it more efficient for  string manipulation.

```
StringBuilder sb = new StringBuilder("Hello");

sb.append(" ").append("World!");  
// sb is now "Hello World!"

sb.replace(0, 5, "Hi");
// sb is now "Hi World!"

```

Other methods:  `insert()`,  `delete()`,  `reverse()`,  `capacity()`  etc.

Call  `toString()`  to get a  `String`  from the  `StringBuilder`.

# Composition

Composition is a type of relationship between classes where one class contains another class as a member variable.

## Key Points

### Life cycle

A composed object's  life cycle  is dependent on the composing object. When the composing object is destroyed, so is the  composed object.

### "Has-a" relationship

Composition denotes a "has-a" relationship between classes. The composing class "has-a" member of the composed class.

### Reuse

Composition allows objects to be reused by many composing objects. The composed object can be reused by many different composing objects.

### Parent-child relationship

Composition  creates a parent-child relationship between classes, where the  composing class  is the parent and composed class is the child.

### Access

Composed objects are accessible via a member variable of the composing object. The composing object can access methods and properties of the composed object.

### Abstraction  and modularity

Objects are composed to achieve abstraction and modularity. Complex classes can be broken down into smaller, focused classes and composed together.

## Examples

-   A Car has an Engine
-   An Engine has an IgnitionSystem
-   An  IgnitionSystem  has  SparkPlugs

## Your Examples

-   The  `Car`  class composes an  `Engine`  by having an  `engine`  member variable.
-   The  `Engine`  class composes an  `IgnitionSystem`  by having an  `ignition`  member variable.
-   The  `IgnitionSystem`  composes a  `SparkPlug`  by having a  `sparkPlug`  member variable.

## In Summary

Composition is a relationship where one class has a member variable of another class, denoting that it "has-a" that class as a part. This allows for abstraction, reuse and modularity in object-oriented design.

## Composition Part 1

The  `Car`  class composes an  `Engine`  to demonstrate a basic level of composition.

```
public class Car {
    private Engine engine;
    
    public Car(Engine engine) {
        this.engine = engine;  
    }
    
    public void startEngine() {
        engine.start();
    }   
}

public class Engine {
    public void start() {
        System.out.println("Engine started!");    
    }
}

```

The  `Car`  class has an  `Engine`  member variable, showing that a car has an engine. When the car's engine is started, it calls the  `start()`  method on the composed  `Engine`  object.

## Composition Part 2

The  `Engine`  class now composes an  `IgnitionSystem`.

```
public class Engine {
    private IgnitionSystem ignition;
    
    public Engine(IgnitionSystem ignition) {
       this.ignition = ignition;    
    }   
      
    public void start() {
        ignition.ignite();     
    }  
}

public class IgnitionSystem {
   public void ignite() {
       // ignite spark plugs
   }    
}

```

The  `Engine`  class has an  `IgnitionSystem`  member variable, demonstrating composition. When the engine is started, it calls the  `ignite()`  method on the composed  `IgnitionSystem`  object.

## Composition Challenge

The  `IgnitionSystem`  now composes a  `SparkPlug`  to demonstrate a deeper level of composition.
```
public class SparkPlug {
   // ...
}

public class IgnitionSystem {
   private SparkPlug sparkPlug;
   // ...   
}

```

The  `IgnitionSystem`  has a  `SparkPlug`  member variable, composing the  spark plug  as a part. This shows multiple levels of composition, with classes composing other classes.
# Encapsulation in Java

Encapsulation is a fundamental concept in object-oriented programming that involves combining data and behavior into a single unit called a class. Encapsulation allows you to control the access to the data and behavior of an object, ensuring that they are used only in the intended way. In Java, encapsulation is achieved through the use of  access modifiers  and getter and  setter methods.

## Access Modifiers

Access modifiers are keywords that determine the accessibility of a class, method, or variable. In Java, there are four types of access modifiers:

-   `public`: The  `public`  modifier makes a class, method, or variable accessible from anywhere in the program.
-   `private`: The  `private`  modifier makes a class, method, or variable accessible only within the same class.
-   `protected`: The  `protected`  modifier makes a class, method, or variable accessible within the same class or any subclass of that class.
-   `default`: If no access modifier is specified, the class, method, or variable has  default accessibility, which means it can be accessed within the same package.

Access modifiers are used to enforce encapsulation by controlling the visibility of data and behavior.

### Example

```
public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}

```

In this example, we have a  `Person`  class with two private member variables:  `name`  and  `age`. The class also has getter and setter methods for both variables, which allow controlled access to the data.

## Getter and Setter Methods

Getter and setter methods are public methods used to access and modify the values of  private member variables. The  naming convention  for getter and setter methods is to prefix the name of the variable with "get" or "set", respectively, and use  camel case  for the rest of the name.

### Example

```
public class Circle {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    public double getRadius() {
        return radius;
    }

    public void setRadius(double radius) {
        if (radius < 0) {
            throw new IllegalArgumentException("Radius cannot be negative");
        }
        this.radius = radius;
    }

    public double getArea() {
        return Math.PI * radius * radius;
    }
}

```

In this example, we have a  `Circle`  class with a private member variable  `radius`. The class has getter and setter methods for the  `radius`  variable, which allows controlled access to the data. The  setter method  also performs  input validation  to ensure that the radius is not negative.

## Encapsulation Challenge

Let's say we have a  `BankAccount`  class with the following requirements:

-   The account balance should not be directly accessible from outside the class.
-   The account balance should be initialized to 0 when a new account is created.
-   The class should have methods to deposit and withdraw from the  account balance.
-   The class should have a method to display the account balance.

### Solution


```
public class BankAccount {
    private double balance;

    public BankAccount() {
        balance = 0;
    }

    public void deposit(double amount) {
        if (amount < 0) {
            throw new IllegalArgumentException("Amount cannot be negative");
        }
        balance += amount;
    }

    public void withdraw(double amount) {
        if (amount < 0) {
            throw new IllegalArgumentException("Amount cannot be negative");
        }
        if (amount > balance) {
            throw new IllegalArgumentException("Insufficient balance");
        }
        balance -= amount;
    }

    public void displayBalance() {
        System.out.println("Account balance: " + balance);
    }
}

```

In this solution, we have a  `BankAccount`  class with a private member variable  `balance`. The class has a  default constructor  that initializes the balance to 0. The class also has deposit and  withdraw methods  that update the balance, and a  displayBalance method  that prints the balance to the console. The deposit and withdraw methods also perform input validation to ensure that the amount is not negative and that the account has sufficient balance for a withdrawal. The balance is not directly accessible from outside the class, enforcing encapsulation.

# Polymorphism in Java

Polymorphism means "many forms" and it occurs when we have classes that are related by inheritance.

## Method Overloading

-   It is a  compile time  polymorphism.
-   Methods have the same name but different parameters.
-   Different signatures.

```
class Overloading{  
  void sum(int a, int b){  
    System.out.println(a+b);
  }

  void sum(int a, int b, int c){
    System.out.println(a+b+c); 
  }
}

```

## Method Overriding

-   It is a  runtime polymorphism.
-   Methods have the same name and signature.
-   Overridden in subclass.
```
class Animal{  
  void makeSound(){
    System.out.println("Making animal sound!");
  }
}

class Dog extends Animal{
  void makeSound(){
    System.out.println("Bark! Bark!");
  }
}

```

## Polymorphism example
```
Animal a = new Dog();  
a.makeSound(); // Prints Bark! Bark!

Animal a2 = new Animal();  
a2.makeSound(); // Prints Making animal sound!

```

Here  `a`  is referring to an  `Animal`  object but it is actually an instance of  `Dog`  class. So the  `Dog`  implementation of  `makeSound()`  is called - demonstrating runtime polymorphism.

# Testing the  runtime type  using instanceof

The  `instanceof`  operator in Java is used to test if an object is an instance of a class, interface, array etc.

Syntax:

`object instanceof Class`

This returns  `true`  if the object is an instance of the specified type, else  `false`.

Example:
```
Animal a = new Dog();

if(a instanceof Animal){
  System.out.println("a is an Animal"); // prints a is an Animal 
}

if(a instanceof Dog){
  System.out.println("a is a Dog"); // prints a is a Dog
}

```

Here  `a`  is a  `Dog`  object but refers to an  `Animal`  type. So both checks return  `true`.

We can use  `instanceof`  to check the runtime type of a polymorphic reference. This allows us to cast the reference to the actual type and  call methods  specific to that type.
```
if(a instanceof Dog){
  Dog d = (Dog) a; 
  d.bark(); // we can call bark() after casting
}

```

So in summary,  `instanceof`  allows us to:

-   Check the runtime type of a  polymorphic reference
-   Perform a typecast
-   Call methods specific to that type
# Arrays

Arrays are objects that store multiple values of the same data type.

## Array Declaration

We declare an array as:

`dataType[] arrayName;`

For example:

`int[] numbers;`  
`String[] names;`

## Array Initialization

We initialize an array either:

-   With size:

`dataType[] arrayName = new dataType[size];`

For example:

`int[] numbers = new int[5];`  
`String[] names = new String[10];`

-   With values:

`dataType[] arrayName = {value1, value2, ...}`

For example:

`int[] numbers = {1, 2, 3};`  
`String[] names = {"John", "Jane", "Jack"};`

## Accessing Array Elements

We access  array elements  using the index inside square brackets:

`arrayName[index]`

For example:

`numbers[0]`  // First element  
`names[2]`  // Third element

## java.util.Arrays class

The  `java.util.Arrays`  class provides several useful methods:

-   `sort()`  - Sorts the elements of the given array

```
int[] numbers = {5, 2, 1, 8};
Arrays.sort(numbers);
// numbers is now {1, 2, 5, 8}

```

-   `fill()`  - Fills the given array with a specified value


```
Arrays.fill(numbers, 0);
// numbers is now {0, 0, 0, 0}

```

-   `copyOf()`  - Creates a copy of the given array


```
int[] numbersCopy = Arrays.copyOf(numbers, numbers.length);

```
# Finding a Match Using  Linear Search

We can find a match in an array using a linear search:

```
int findMatch(int[] arr, int match) {
  for (int i = 0; i < arr.length; i++) {
     if (arr[i] == match) {
       return i;  
     }    
  }
  return -1;  // Not found    
}

```

This searches each element in the array until it finds a match.

Time complexity: O(n)

# Using Binary Search

We can perform a faster search using binary search:
```
int binarySearch(int[] arr, int key) {
  int low = 0; 
  int high = arr.length - 1;
  
  while (low <= high) {
     int mid = (low + high) / 2;
     if (key < arr[mid]) {
        high = mid - 1;        
     } else if (key > arr[mid]) {
         low = mid + 1;         
     } else {
         return mid;           
     }    
  }
  return -1;  
}

```

This divides the array in half on each iteration, speeding up the search.

Time complexity: O(log n)

# Comparing Arrays

We can compare two arrays for equality using a deep comparison:

```
boolean arraysEqual(int[] a, int[] b) {
   if (a.length != b.length) return false;
   for (int i = 0; i < a.length; i++) {
      if (a[i] != b[i]) return false;
   }
   return true;      
} 

```
# Arrays Recap

Arrays in Java are data structures used to store a fixed-size sequence of elements of the same type. They provide a convenient way to store and access multiple values of the same data type. Here is a recap of arrays in Java, along with examples:

## Declaration and Initialization

To declare an array, you specify the type of the elements followed by square brackets (`[]`) and then the array name. For example, to declare an array of integers:


`int[] numbers;` 

To initialize an array, you can either specify the size of the array or provide the initial values:


`int[] numbers = new int[5];  // Initializes an array of size 5 with default values (0 for integers)
int[] primes = {2, 3, 5, 7, 11};  // Initializes an array with the specified values` 

## Accessing Array Elements

You can access individual elements of an array using the index, which starts from 0. For example:


```
int[] numbers = {10, 20, 30, 40, 50};

int firstNumber = numbers[0];  // Accesses the first element (10)
int thirdNumber = numbers[2];  // Accesses the third element (30)
```

## Array Length

The `length` property of an array gives you the number of elements it can hold. For example:


```
int[] numbers = {10, 20, 30, 40, 50};

int length = numbers.length;  // Gives the length of the array (5)
``` 

## Looping through an Array

You can use a loop, such as a `for` loop, to iterate over the elements of an array. For example:


```
int[] numbers = {10, 20, 30, 40, 50};

for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
``` 

This loop prints each element of the array on a new line.

## Arrays as Method Parameters

Arrays can be passed as parameters to methods. When you pass an array to a method, the method receives a reference to the array, allowing it to modify the array if needed. For example:


```
void modifyArray(int[] array) {
    array[0] = 100;
}

int[] numbers = {10, 20, 30};
modifyArray(numbers);
System.out.println(numbers[0]);  // Prints 100
``` 

In this example, the `modifyArray` method changes the value of the first element of the array.

These are some basic concepts related to arrays in Java. Arrays are widely used for storing and manipulating collections of data in a structured manner.

# References Types vs Value Types

In Java, variables can be categorized into two types: reference types and value types. Understanding the difference between these two types is crucial for working with Java effectively. Here's a detailed explanation with examples:

## Value Types

Value types, also known as primitive types, store the actual values. When you declare a value type variable, the variable directly holds the value itself. Examples of value types in Java include `int`, `double`, `boolean`, etc. Let's consider an example:


```
int x = 5;
int y = x;
y = 10;
System.out.println(x);  // Outputs 5
System.out.println(y);  // Outputs 10
``` 

In this example, the value of `x` is copied to `y`, and modifying `y` doesn't affect the value of `x`. Value types are independent of each other.

## Reference Types
Reference types, also known as objects, store references or addresses to the actual objects in memory. When you declare a reference type variable, the variable holds a memory address pointing to the location where the object is stored. Examples of reference types in Java include arrays, classes, and interfaces. Let's consider an example:


```
int[] array1 = {1, 2, 3};
int[] array2 = array1;
array2[0] = 10;
System.out.println(array1[0]);  // Outputs 10
System.out.println(array2[0]);  // Outputs 10
``` 

In this example, `array1` and `array2` both refer to the same memory location. Modifying `array2` also affects the value of `array1`. Reference types are not independent of each other; they refer to the same underlying object.

## Passing Variables to Methods

When you pass a value type variable to a method, a copy of the variable is passed, and modifications made within the method do not affect the original variable. Consider the following example:


```
void modifyValue(int value) {
    value = 10;
}

int x = 5;
modifyValue(x);
System.out.println(x);  // Outputs 5
``` 

In this example, modifying `value` within the method does not change the value of `x` because `value` is a copy of `x`.

When you pass a reference type variable to a method, the reference (memory address) is passed. Modifying the referenced object within the method affects the original object. Consider the following example:


```
void modifyArray(int[] array) {
    array[0] = 10;
}

int[] numbers = {1, 2, 3};
modifyArray(numbers);
System.out.println(numbers[0]);  // Outputs 10
``` 

In this example, modifying the `array` within the method changes the value of `numbers[0]` because `array` and `numbers` both refer to the same array object.

Understanding the distinction between value types and reference types is crucial for proper variable manipulation and passing in Java. It helps avoid confusion and ensures accurate results when working with variables in different contexts.

# Variable Arguments (Varargs)

In Java, variable arguments, or varargs, allow methods to accept a variable number of arguments of the same type. Varargs provide flexibility when you need to pass a different number of arguments to a method. Here's a detailed explanation with examples:

## Syntax

To define a method with variable arguments, you use an ellipsis (`...`) after the parameter type. The varargs parameter is treated as an array inside the method. Here's the syntax:


`return_type method_name(type... parameter_name) {
    // Method implementation
}` 

## Usage

Varargs are useful when you want to pass a variable number of arguments to a method without explicitly defining an array. Let's consider an example where we want to find the maximum of multiple numbers:


```
int findMax(int... numbers) {
    int max = Integer.MIN_VALUE;
    for (int num : numbers) {
        if (num > max) {
            max = num;
        }
    }
    return max;
}

int result1 = findMax(5, 10, 15);  // Calls findMax with 3 arguments
int result2 = findMax(2, 4, 6, 8, 10);  // Calls findMax with 5 arguments
``` 

In this example, the `findMax` method accepts a variable number of `int` arguments using varargs. It finds the max element.
## Declaration

Two-dimensional arrays are arrays of arrays. They are declared as:

```
dataType[][] arrayName;

```

For example:
```
int[][] numbers;
String[][] names;  
double[][] values;

```

## Initialization

They can be initialized using:

-   A list of  array initializers:

```
int[][] numbers = { {1,2,3}, {4,5,6}, {7,8,9}};

```

-   The  `new`  operator:

```
int rows = 3;
int cols = 4;
int[][] numbers = new int[rows][cols];

```

This creates a  2D array  of 3 rows and 4 columns.

## Access

Elements are accessed using two indices:

```
numbers[row][col];

```

For example:
```
int value = numbers[1][2]; // Accesses element at row 1, col 2  

```

## Multi-dimensional Arrays

Arrays of higher dimensions are also supported. For example:

```
int[][][] threeD; 

```

This is a three-dimensional array. Elements are accessed as:
```
threeD[x][y][z];

```

The time and  space complexity  of accessing an element is O(1). However, traversing the entire multi-dimensional array has  time complexity  O(n^d) where  `n`  is the size of one dimension and  `d`  is the number of dimensions.
## ArrayList

An ArrayList is a resizable array. It implements the List interface.

Some benefits of ArrayList over arrays are:

-   Automatic expansion  and contraction
-   Easier manipulation of elements using  List interface methods

## Declaration

ArrayList is declared as:

```
import java.util.ArrayList;

ArrayList<Type> listName = new ArrayList<>();

```

Here  `Type`  specifies the type of elements stored in the list.

For example:

```
ArrayList<String> names = new ArrayList<>();
ArrayList<Integer> numbers = new ArrayList<>();

```

## Adding Elements

Elements are added using  `add()`:

```
listName.add(element);

```

For example:

```
names.add("John");
names.add("Jane"); 

```

## Accessing Elements

Elements are accessed using their index:

```
listName.get(index); 

```

For example:

```
String name = names.get(0); // John

```

## Removing Elements

Elements can be removed using:

-   `remove(index)`: Removes element at given index
-   `remove(object)`: Removes specific object from the list

```
listName.remove(index);
listName.remove(object);

```

## Size

The  `size()`  method returns the number of elements:

```
int size = listName.size();
```
