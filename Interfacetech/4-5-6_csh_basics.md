# C# basics

## What?

C# is an oop language developed by Microsoft in the early 2000s, as part of the .NET initiative. It is strongly inspired by Java, C and C++ but builds heavily on features provided by the .NET framework, such as the Common Language Infrastructure and the Common Language Runtime.

## Features

* **Portability** thanks to the **Common Language Infrastructure**
* **Typed**
* **Metaprogramming**
* **Properties**:  syntactic sugar for a common pattern in which a pair of methods, accessor (getter) and mutator (setter) encapsulate operations on a single attribute

### Properties and Fields

Properties expose fields. Fields should (almost always) be kept private to a class and accessed via get and set properties. Properties provide a level of abstraction allowing you to change the fields while not affecting the external way they are accessed by the things that use your class.

```cs
public class MyClass
{
    // this is a field.  It is private to your class and stores the actual data.
    private string _myField;

    // this is a property. When accessed it uses the underlying field,
    // but only exposes the contract, which will not be affected by the underlying field
    public string MyProperty
    {
        get
        {
            return _myField;
        }
        set
        {
            _myField = value;
        }
    }

    // This is an AutoProperty (C# 3.0 and higher) - which is a shorthand syntax
    // used to generate a private field for you
    public int AnotherProperty{get;set;} 
}
```

### Methods

A method is a function associated with a class.

```cs
using System;

abstract class Motorcycle
{
   // Anyone can call this.
   public void StartEngine() {/* Method statements here */ }

   // Only derived classes can call this.
   protected void AddGas(int gallons) { /* Method statements here */ }

   // Derived classes can override the base class implementation.
   public virtual int Drive(int miles, int speed) { /* Method statements here */ return 1; }

   // Derived classes can override the base class implementation.
   public virtual int Drive(TimeSpan time, int speed) { /* Method statements here */ return 0; }

   // Derived classes must implement this.
   public abstract double GetTopSpeed(); 
}
```

### Class

Az objektumorientált programozás (OOP) alapegysége az osztály, amellyel le tudjuk írni egy modellnek a tulajdonságait, viselkedését. Az osztály tehát a metódusok és az adatok (adattagok) halmaza.

```cs
//[access modifier] - [class] - [identifier]
public class Customer
{
   // Fields, properties, methods and events go here...
}

public class Manager : Employee
{
    // Employee fields, properties, methods and events are inherited
    // New Manager fields, properties, methods and events go here...
}
```

```cs
Customer object1 = new Customer();
Customer object2; // no object created; just reference
```

```cs
using System;

public class Person
{
    // Constructor that takes no arguments:
    public Person()
    {
        Name = "unknown";
    }

    // Constructor that takes one argument:
    public Person(string name)
    {
        Name = name;
    }

    // Auto-implemented readonly property:
    public string Name { get; }

    // Method that overrides the base class (System.Object) implementation.
    public override string ToString()
    {
        return Name;
    }
}
class TestPerson
{
    static void Main()
    {
        // Call the constructor that has no parameters.
        var person1 = new Person();
        Console.WriteLine(person1.Name);

        // Call the constructor that has one parameter.
        var person2 = new Person("Sarah Jones");
        Console.WriteLine(person2.Name);
        // Get the string representation of the person2 instance.
        Console.WriteLine(person2);

        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
}
// Output:
// unknown
// Sarah Jones
// Sarah Jones
```

### Types

C# is a strongly-typed language. Every variable and constant has a type, as does every expression that evaluates to a value.

C# provides a standard set of built-in numeric types to represent **integers**, **floating point** values, **Boolean** expressions, text **characters**, **decimal** values, and other types of data. There are also built-in **string** and **object** types.

#### Anonymous type

Anonymous type, as the name suggests, is a type that doesn't have any name. C# allows you to create an object with the new keyword without defining its class. The implicitly typed variable- var is used to hold the reference of anonymous types.

```cs
var myAnonymousType = new { firstProperty = "First", 
    secondProperty = 2, 
    thirdProperty = true 
};
```

#### Generics

Generics are similar to templates from C++. The key difference is that they are resolved at runtime while C++ does this in the build phase.

```cs
List<Person> foo = new List<Person>();
```

#### List

Generic class that represents a strongly typed list of objects that can be accessed by index. Provides methods to search, sort, and manipulate lists.

```cs
List<string> dinosaurs = new List<string>();

Console.WriteLine("\nCapacity: {0}", dinosaurs.Capacity);

dinosaurs.Add("Tyrannosaurus");
dinosaurs.Add("Amargasaurus");
dinosaurs.Add("Mamenchisaurus");
dinosaurs.Add("Deinonychus");
dinosaurs.Add("Compsognathus");
Console.WriteLine();
foreach(string dinosaur in dinosaurs)
{
    Console.WriteLine(dinosaur);
}

Console.WriteLine("\nCapacity: {0}", dinosaurs.Capacity);
Console.WriteLine("Count: {0}", dinosaurs.Count);

Console.WriteLine("\nContains(\"Deinonychus\"): {0}",
    dinosaurs.Contains("Deinonychus"));

Console.WriteLine("\nInsert(2, \"Compsognathus\")");
dinosaurs.Insert(2, "Compsognathus");
```

## Sources

https://en.wikipedia.org/wiki/C_Sharp_(programming_language)
https://en.wikipedia.org/wiki/.NET_Framework
https://stackoverflow.com/questions/295104/what-is-the-difference-between-a-field-and-a-property
https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes
http://www.webelektronika.com/article/2014010620osztalyok_a_csharp_nyelvben_I_resz
https://docs.microsoft.com/en-us/dotnet/csharp/basic-types
http://www.webelektronika.com/article/2014010915Valtozok_a_Csharp_programozasi_nyelvben
https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics
https://stackoverflow.com/a/1208207/2229560
https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1?view=netframework-4.8