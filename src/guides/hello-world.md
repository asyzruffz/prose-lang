# Hello, World!

Welcome to your first Prose program! In this tutorial, you'll create a new Prose project and write the traditional "Hello, World!" program.

## Creating a New Project

Before writing any Prose code, you need to create a new project using the `stitch` program. First, make sure you have access to the `stitch` executable.

    stitch --version

Create a new project called "hello-world":

```bash
stitch new hello-world
```

This command will create a new project structure:
- `Book.toml` - Project configuration file
- `source/` directory - Contains your Prose source files
- `source/main.prs` - Main entry point for your program
- `intermediate/` directory - Contains compiled intermediate files

## Project Structure

After creating the project, your directory structure will look like this:

```
hello-world/
├── source/
│   └── main.prs
└── Book.toml
```

- **`Book.toml`** - Contains project metadata like name and version
- **`source/main.prs`** - Your main Prose source file

## Writing Your First Program

Navigate to your project directory and open `source/main.prs`. Replace the default content with:

```prose path=null start=null
lore print "Hello, World!".
```

That's it! This single line is a complete Prose program.

## Running the Program

To run your program, use the `stitch run` command from your project directory:

```bash
stitch run
```

You should see the following output:

```
Hello, World!
```

## Understanding the Code

Let's break down what's happening in this simple program:

- **`lore`** - This is the built-in scope that provides access to standard library functions
- **`print`** - This is a verb (function) that outputs text to the console  
- **`"Hello, World!"`** - This is a text literal (string) that we want to display
- **`.`** - Every sentence (statement) in Prose ends with a period, just like in English

## A More Complex Example

Let's create a slightly more elaborate program. Edit your `source/main.prs` file:

```prose path=null start=null
so name is text as "World".
lore print "Hello, " and name and "!".
```

This program:
1. Defines a variable `name` of type `text` with the value "World"
2. Prints a greeting using string concatenation with the `and` operator

Run it again with `stitch run` to see the output.

## Variables and Types

Prose uses the `so` keyword to define variables. The syntax is:

```prose path=null start=null
so <variable_name> is <type> as <value>.
```

For example:
```prose path=null start=null
so age is number as 25.
so greeting is text as "Hello there!".
```

## Interactive Example

Here's a more interactive example that shows how Prose reads like natural language. Replace your `main.prs` content with:

```prose path=null start=null
noun person {
    so name is text.
    so age is number.
    
    verb greet {
        lore print "Hello, my name is " and it name and "!".
    }
}

so alice is person.
alice name as "Alice".
alice age as 30.
alice greet.
```

This program:
1. Defines a `person` noun (struct) with `name` and `age` properties
2. Adds a `greet` verb (method) to the person
3. Creates an instance called `alice`
4. Sets Alice's properties
5. Calls the greet method

## Building Your Project

You can also build your project to generate intermediate files without running it:

```bash
stitch build
```

To clean up generated files:

```bash
stitch clean
```

To clean and rebuild:

```bash
stitch rebuild
```

## What's Next?

Congratulations! You've created your first Prose project and written your first programs. Here are some suggestions for what to explore next:

- Learn about [Basic Concepts](basic-concepts.md) to understand Prose's core principles
- Explore [Nouns](features/nouns.md) to create custom data types
- Discover [Verbs](features/verbs.md) to write functions and methods
- Check out the [Standard API](standard-api.md) to see what's available in the `lore` scope

## Exercises

Try these exercises to practice what you've learned:

1. **Personal Greeting**: Create a program that prints your name and age
2. **Simple Calculator**: Write a program that adds two numbers and prints the result
3. **Pet Introduction**: Create a `pet` noun with name and species, then make your pet introduce itself

Remember to use `stitch run` to test your programs and `stitch clean` to clean up when needed.

Happy coding in Prose!
