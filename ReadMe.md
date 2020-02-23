# Software Engineering Fundamentals in C# - Part 1
## Hello World!
- created  a console application
- all console appplications include:
* one or more namespace
* one or more class
* only one Main method

## Using Statements


# C# Essential Training - Part 1
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
- Working with constants and enumerators
    - variables declared with const
    - enum
- Working with Dates and Times

### Working with Classes
- Creating a Class
- 

// C# E T 2
## Unit Testing and Test Driven Development
- What is Unit Testing?
    - TDD code deved in phases
    - create or change -> Create Reproduceable Test -> Review the Results
    - goal = 100% coveage
- Cereate unit test project

## Arrays and Collections
- Simple Arrays
    - strongly typed, need to be specific of types in array and be consistent.
    - arrays have fixed size
    ``` C#
        var myArray = new string[4];
        myArray[0] = "First Item";
        myArray[5] = "outside Item"; // throws error out of bounds
    ```
- Resizing arrays
    - 
    ``` C#
        var myArray = new string[4] { "First", "Second", "Third", "Fourth"};
        myArray[2] // "Third"
        myArray[5] // error
        Array.Resize(ref myArray, 6);
        myArray[5] = "Fourth";
        myArray[6] = "Fifth";
    ```
    - ref allows to pass in things by reference and modify them directly rather than a copy of them
- Working with simple arrays
    - 
- MultiDimensional Arrays
    - 
    ``` C#
        var multi = new int[3,4] {
            {0,1,2,3},
            {4,5,6,7},
            {8,9,10,11}
        }
        multi[2,3]  // 11
        multi[0,0] // 0
        multi[1,1] // 5
    ```
- Managing Ordered Data Lists
    - lists are part of a class called generic collections
        ``` C#
        var awesomeSauces = new list<string>();
        awesomeSauce.Add("tobasco", "chalula")
        awesomeSauces.[0] // tobasco
    ```
    - Don't need to resize or specify a size for list
- Working with Lists
    - 
- testing the List implementation
    - 
- Introduction to LInQ
    - Language Integration Query
    - a set of extension classes
    - method that will extend an existing class without subclassing it or altering codeof the class itself
    - 
    ``` C#
        var listNumbers = new int[5] {
            1,3,5,7,9
        };
        listNumbers.Sum() // 25
        listNumbers.Average() // 5
        listNumbers.Where( item => item >= 3) // 3 , 5, 7, 9
    ```
- Unordered data and dictionaries
    - keys must be unique
    ``` C#
        var new dictionaryWords = new Dictionary<string, string>();
        dictionaryWords.add("var", "shorthand for variable");
        dictionaryWords["var"] // shorthand for variable
        dictionaryWords.add("var", "something else"); // error
    ```

## Flow Control
- Evaluating with if/else
- The forEach Loop
    ``` c#
    public int ForEachLoop()
    {
        var numbers = new List<int> {1,3,5,7,9};
        var sum = 0;
        foreach(var number in numbers) 
        {
            sum = sum + number;
        }
        return sum;
    }
    ```
- Break and Continue
    - can use break and continue to alter loops
    - continue will stop current iteration of loop and go to next iteration in loop
    - break will exit entire loop 

## Exception Handling
- Adding a console project
- Understanding runtime Exceptions
    - occurs when mistakein your code not caught by compiler
- debugging exceptions in your code
    - clicking gray area left of line number will place a breakpoint in the program to debug code in execution at that point
    - allows to inspect the values in scopeat that point
    - allows to step through execution
- handling errors with try catch
- Multiple catch statements
    - paraenthesis after catch allows to specify errors to catch
- cleaning up with finally statement
    - finally runs regardless of conditions

