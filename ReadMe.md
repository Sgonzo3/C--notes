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
- Concatenation
    - + will concatenate two strings
    - StringBuilder
    ```cs
    var sb = new StringBuilder();
    sb.Append("It was the best of times, it was the worst of times");
    sb.Append("It was the age of wisdom");
    sb.Append("It was the age of foolishness");
    sb.ToString()

    var sb = new StringBuilder();
    sb.AppendLine("It was the best of times, it was the worst of times");
    sb.AppendLine("It was the age of wisdom");
    sb.AppendLine("It was the age of foolishness");
    sb.ToString()
    ```
- String formatters
    - 
    ```c#
        var city = "Dallas";
        var temp = 103.4f;
        var currentDateTime = DateTime.Now;

        string.Format("Welcome to {0}. The time is {1}. The temperature is {2}.", city, currentDateTime, temp) // Welcome to Dallas. The time is TIME. The temperature is 103.4.
    ```
- Parsing Strings as Numbers
    ```c#
        var test= "15,234";
        int.Parse(test.Replace(",","")) // 15234
    ```
- Math in C#
    - Math.Abs(-5) // 5 
        - gives absolute value
    - Math.Pow()
    - Math.Round() returns estimate value
    - Math.Floor() retrurns nearest low estimate
    - Math.Ceiling returns nearest high estimate