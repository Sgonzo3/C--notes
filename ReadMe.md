# Software Engineering Fundamentals in C# - Part 1
## Hello World!
- created  a console application
- all console appplications include:
* one or more namespace
* one or more class
* only one Main method

## Using Statements


## Namespace
- classes are organized into Namespaces
- allow dev to organize code
- prevents classes with same names from being ambiguous

## Defining Variables
- Strongly typed, must define type while declaring variable
- string firstString = "Some text";
- var secondString = " Some other text";
- - if assigning at declaration and using var C# will use implicit typing to determine type
- Ending line without semicolon will execute in interactive window

## Built-in Data Types
- Strings: must use double quotes
- single quotes represent char Characters
- Integer: 32bit signed int, uint for unsigned int only positive
    - int firstInt = 5;
    - var secondInt = 6;
- float: must end number with f to specify a float
- boolean: 

## Everything is an Object
- PrimitiveType. will list properties and methods listed on the object for any primitive

## Strings
- 
```C#
     var testString = " abcdefg";
     testString.Trim() // "abcdefg";
     var challenge = " Text processing in C# is really great!  ";
     challenge.Trim().Substring(24,challenge.trim().length - 25).ToUpper().Trim()
```