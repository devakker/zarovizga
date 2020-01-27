# CRUD .net 3.0

## What is CRUD?

In computer programming, create, read, update, and delete (CRUD) are the four basic functions of persistent storage.

## CRUD in .net

### Creating a model

A data model can be used to manage instances of items in a database connected to our application. 

```cs
using System;
using System.ComponentModel.DataAnnotations;

namespace RazorPagesMovie.Models
{
    public class Movie
    {
        public int ID { get; set; }
        public string Title { get; set; }

        [DataType(DataType.Date)]
        public DateTime ReleaseDate { get; set; }
        public string Genre { get; set; }
        public decimal Price { get; set; }
    }
}
```

### Scaffolding

The previously defined model has to be scaffolded in order to generate the CRUD operations. Scaffolding is done trough Visual Studio and it will create the following files:

* Pages/Movies: Create, Delete, Details, Edit, and Index.
* `Data/RazorPagesMovieContext.cs`

It will also update the `Startup.cs` file

### Initial migration

A data model changes during development and gets out of sync with the database. You can drop the database and let EF create a new one that matches the model, but this procedure results in the loss of data. The migrations feature in EF Core provides a way to incrementally update the database schema to keep it in sync with the application's data model while preserving existing data in the database.

Using the Package Manager Console a migration has to performed and the database has to be updated:

```
Add-Migration InitialCreate
Update-Database
```

## Sources

https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/model?view=aspnetcore-3.1&tabs=visual-studio
https://docs.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=dotnet-core-cli