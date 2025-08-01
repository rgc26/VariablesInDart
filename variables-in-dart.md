author: Dart Tutorial Team
summary: Learn about variables, data types, constants, and naming conventions in Dart programming
id: variables-in-dart
categories: codelab,markdown,programming,dart
environments: Web
status: Published
feedback link: https://github.com/your-repo
analytics account: Google Analytics ID

# Variables in Dart Tutorial

## Overview
Duration: 0:02:00

Welcome to the Variables in Dart Tutorial! This codelab will teach you everything you need to know about variables in Dart programming language. Variables are fundamental building blocks that allow you to store and manipulate data in your programs.

**What you'll learn:**
* Understanding what variables are and how they work
* Different variable types and data types in Dart
* Proper syntax for declaring variables
* Rules for creating valid variable names
* Working with constants using `const` keyword
* Naming conventions and best practices

**Prerequisites:**
* Basic understanding of programming concepts
* Familiarity with Dart syntax (from Basic Dart Program tutorial)

Positive
: This tutorial builds upon the basic Dart concepts and will help you write more structured and maintainable code!

## Understanding Variables
Duration: 0:03:00

Variables are containers used to store values in your program. Think of them as labeled boxes where you can put different types of data that you want to use later.

### What are Variables?

Variables are named storage locations that can hold different types of data. Here's a simple example:

```dart
// here variable name contains value John.
var name = "John";
```

In this example:
* `name` is the variable name
* `"John"` is the value stored in the variable
* `var` is the keyword that tells Dart to create a variable

### Why Use Variables?

Variables are essential because they allow you to:
* Store data for later use
* Make your code more readable and maintainable
* Perform calculations and operations on data
* Reuse values throughout your program

Positive
: Variables make your code dynamic and flexible - you can change their values as your program runs!

## Variable Types and Data Types
Duration: 0:05:00

Dart supports several data types that determine what kind of values a variable can store. Understanding these types is crucial for writing effective Dart code.

### Basic Data Types in Dart

Here are the main data types you'll work with:

* **String**: For storing text values (must be in quotes)
  * Examples: `"John"`, `"Hello World"`, `"123"`
* **int**: For storing integer values (whole numbers)
  * Examples: `10`, `-10`, `8555`
* **double**: For storing floating-point values (decimal numbers)
  * Examples: `10.0`, `-10.2`, `85.698`
* **num**: For storing any type of number (both int and double)
  * Examples: `10`, `20.2`, `-20`
* **bool**: For storing true or false values
  * Examples: `true`, `false`
* **var**: For storing any value (type inference)
  * Examples: `'Bimal'`, `12`, `'z'`, `true`

### Syntax for Creating Variables

The basic syntax for creating a variable in Dart is:

```dart
type variableName = value;
```

For example:
```dart
String name = "John";
int age = 25;
double height = 5.9;
bool isStudent = true;
```

Negative
: Remember that Dart is strongly typed, so once you declare a variable with a specific type, you can only assign values of that type to it!

## Working with Variables - Examples
Duration: 0:05:00

Let's see how to declare variables and use them in practice with a comprehensive example.

### Example: Using Variables in Dart

```dart
void main() {
// declaring variables
String name = "John";
String address = "USA";  
num age = 20; // used to store any types of numbers 
num height = 5.9;
bool isMarried = false;
   
// printing variables value   
print("Name is $name");
print("Address is $address");
print("Age is $age");
print("Height is $height");
print("Married Status is $isMarried");
}
```

**Output:**
```
Name is John
Address is USA
Age is 20
Height is 5.9
Married Status is false
```

### Key Points from the Example

* We declared variables of different types: `String`, `num`, and `bool`
* We used string interpolation (`$variableName`) to include variables in our output
* The `num` type can store both integers and floating-point numbers
* Each variable has a descriptive name that indicates its purpose

Positive
: Always use descriptive variable names. Don't use names like `a`, `b`, `c` as they make your code harder to understand and maintain!

## Rules for Creating Variables
Duration: 0:04:00

Dart has specific rules for creating valid variable names. Following these rules is essential to avoid compilation errors.

### Variable Naming Rules

1. **Case Sensitivity**: Variable names are case sensitive
   * `name` and `Name` are different variables
   * `age` and `Age` are different variables

2. **Allowed Characters**: Variable names can consist of:
   * Letters (a-z, A-Z)
   * Numbers (0-9)
   * Underscore (_)
   * Dollar sign ($)

3. **Starting Character**: Variable names cannot start with a number
   * ✅ Valid: `name1`, `age_2`, `$price`
   * ❌ Invalid: `1name`, `2age`, `3price`

4. **Keywords**: Dart keywords cannot be used as variable names
   * ❌ Invalid: `var`, `const`, `final`, `if`, `for`, etc.

5. **No Spaces**: Blank spaces are not allowed in variable names
   * ❌ Invalid: `first name`, `user age`
   * ✅ Valid: `firstName`, `userAge`, `first_name`

6. **Special Characters**: Only underscore (_) and dollar ($) are allowed
   * ❌ Invalid: `name@`, `age#`, `price%`
   * ✅ Valid: `user_name`, `$price`, `age_2`

### Examples of Valid and Invalid Names

```dart
// Valid variable names
String firstName = "John";
int userAge = 25;
double price_2 = 99.99;
String $currency = "USD";

// Invalid variable names (will cause errors)
// String first name = "John";  // spaces not allowed
// int 1age = 25;              // cannot start with number
// double price@ = 99.99;      // special characters not allowed
// String var = "test";        // keyword not allowed
```

Negative
: Breaking these rules will cause compilation errors, so always follow the naming conventions!

## Constants in Dart
Duration: 0:04:00

Sometimes you need to store values that should never change during the program's execution. These are called constants.

### What are Constants?

Constants are variables whose values never change once they are assigned. In programming:
* **Mutable** values can be changed
* **Immutable** values cannot be changed

### Using the `const` Keyword

To create a constant in Dart, use the `const` keyword:

```dart
void main(){
const pi = 3.14;
// pi = 4.23; // This would cause an error - constants cannot be reassigned
print("Value of PI is $pi");
}
```

**Output:**
```
Value of PI is 3.14
```

### When to Use Constants

Use constants for values that should never change, such as:
* Mathematical constants (π, e)
* Configuration values
* Fixed application settings
* Magic numbers that have specific meanings

### Example: Constants in Practice

```dart
void main() {
  const double PI = 3.14159;
  const String APP_NAME = "My Calculator";
  const int MAX_ATTEMPTS = 3;
  
  print("Application: $APP_NAME");
  print("PI value: $PI");
  print("Maximum login attempts: $MAX_ATTEMPTS");
  
  // These would cause errors:
  // PI = 3.14;           // Error: Constant variables can't be assigned
  // APP_NAME = "New App"; // Error: Constant variables can't be assigned
}
```

Positive
: Using constants makes your code more maintainable and prevents accidental changes to important values!

## Naming Conventions
Duration: 0:03:00

Following proper naming conventions makes your code more readable and professional. Dart has specific conventions that you should follow.

### LowerCamelCase Convention

In Dart, variable names should follow the **lowerCamelCase** convention:
* Start with a lowercase letter
* Capitalize the first letter of each subsequent word
* No spaces or special characters between words

### Examples of Good Naming

```dart
// Good naming conventions
String firstName = "John";
String lastName = "Doe";
int userAge = 25;
double accountBalance = 1000.50;
bool isActive = true;
String emailAddress = "john@example.com";

// Avoid these naming styles
String firstname = "John";     // missing capital
String last_name = "Doe";      // using underscore
int user_age = 25;            // using underscore
double AccountBalance = 1000.50; // starting with capital
```

### Naming Convention Examples

```dart
// Not standard way
var fullname = "John Doe";
var user_age = 25;
var EMAIL = "john@example.com";

// Standard way (lowerCamelCase)
var fullName = "John Doe";
var userAge = 25;
var email = "john@example.com";
const pi = 3.14;
```

### Best Practices for Variable Names

1. **Be Descriptive**: Choose names that clearly indicate the variable's purpose
   * ✅ Good: `userAge`, `productPrice`, `isLoggedIn`
   * ❌ Poor: `a`, `x`, `temp`

2. **Use Appropriate Length**: Not too short, not too long
   * ✅ Good: `firstName`, `accountBalance`
   * ❌ Too short: `fn`, `bal`
   * ❌ Too long: `userFirstNameFromDatabase`

3. **Be Consistent**: Use the same naming style throughout your code
   * If you use `firstName`, also use `lastName`, not `last_name`

Positive
: Good naming conventions make your code self-documenting and easier for other developers to understand!

## Practice Exercise
Duration: 0:04:00

Now it's time to practice what you've learned about variables in Dart!

### Exercise: Student Information System

Create a Dart program that stores and displays student information using proper variable types and naming conventions.

**Requirements:**
1. Declare variables for student name, age, grade, and enrollment status
2. Use appropriate data types for each variable
3. Follow proper naming conventions
4. Use constants for fixed values
5. Display all information using string interpolation

### Sample Solution

```dart
void main() {
  // Constants
  const String SCHOOL_NAME = "Dart Academy";
  const int MIN_AGE = 16;
  
  // Student information variables
  String studentName = "Alice Johnson";
  int studentAge = 18;
  double studentGrade = 92.5;
  bool isEnrolled = true;
  String studentEmail = "alice.johnson@dartacademy.com";
  
  // Display student information
  print("=== Student Information ===");
  print("School: $SCHOOL_NAME");
  print("Name: $studentName");
  print("Age: $studentAge");
  print("Grade: $studentGrade%");
  print("Enrolled: $isEnrolled");
  print("Email: $studentEmail");
  print("Minimum age requirement: $MIN_AGE");
  
  // Calculate and display additional information
  bool meetsAgeRequirement = studentAge >= MIN_AGE;
  print("Meets age requirement: $meetsAgeRequirement");
}
```

**Expected Output:**
```
=== Student Information ===
School: Dart Academy
Name: Alice Johnson
Age: 18
Grade: 92.5%
Enrolled: true
Email: alice.johnson@dartacademy.com
Minimum age requirement: 16
Meets age requirement: true
```

Negative
: Try to solve this exercise on your own before looking at the solution!

Positive
: Practice is the best way to master variable concepts in Dart!

## Common Mistakes to Avoid
Duration: 0:02:00

Let's look at some common mistakes beginners make with variables and how to avoid them.

### Common Variable Mistakes

1. **Forgetting Semicolons**
   ```dart
   // ❌ Wrong
   String name = "John"
   
   // ✅ Correct
   String name = "John";
   ```

2. **Using Wrong Data Types**
   ```dart
   // ❌ Wrong - trying to assign string to int
   int age = "25";
   
   // ✅ Correct
   int age = 25;
   ```

3. **Poor Variable Names**
   ```dart
   // ❌ Poor naming
   String n = "John";
   int a = 25;
   
   // ✅ Good naming
   String name = "John";
   int age = 25;
   ```

4. **Not Using Constants for Fixed Values**
   ```dart
   // ❌ Poor - magic numbers
   double area = 3.14159 * radius * radius;
   
   // ✅ Better - using constant
   const double PI = 3.14159;
   double area = PI * radius * radius;
   ```

5. **Ignoring Case Sensitivity**
   ```dart
   // ❌ Wrong - these are different variables
   String name = "John";
   print(Name); // Error: Name is not defined
   
   // ✅ Correct
   String name = "John";
   print(name);
   ```

Positive
: Being aware of these common mistakes will help you write better Dart code from the start!

## Next Steps
Duration: 0:02:00

Congratulations! You've completed the Variables in Dart Tutorial. Here's what you've accomplished:

### What You've Learned

* ✅ Understanding of what variables are and their purpose
* ✅ Knowledge of different data types in Dart
* ✅ Proper syntax for declaring variables
* ✅ Rules for creating valid variable names
* ✅ Working with constants using `const`
* ✅ Following naming conventions (lowerCamelCase)
* ✅ Best practices for variable usage

### Continue Your Learning Journey

To expand your Dart knowledge, consider learning about:

* **Data Types in Dart** - More detailed coverage of all data types
* **Operators in Dart** - How to perform operations on variables
* **Control Flow** - Using variables in conditions and loops
* **Functions** - Passing variables as parameters
* **Collections** - Working with lists, maps, and sets
* **Null Safety** - Dart's null safety features

### Resources

* [Official Dart Documentation](https://dart.dev/guides)
* [Dart Language Tour](https://dart.dev/guides/language/language-tour)
* [Dart Tutorial Website](https://dart-tutorial.com)
* [DartPad](https://dartpad.dev) - Online Dart editor

### Final Challenge

Create a simple calculator program that:
* Declares variables for two numbers and an operation
* Uses appropriate data types for each variable
* Follows proper naming conventions
* Includes constants for mathematical operations
* Displays the result using string interpolation

Positive
: You now have a solid foundation in Dart variables and are ready to tackle more complex programming concepts!

Negative
: Remember to always use descriptive variable names and follow the naming conventions you've learned! 