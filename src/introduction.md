# Introduction

Welcome to **Prose**, a programming language that reads like natural language! Prose is designed to make code more intuitive and expressive by using English-like syntax that closely resembles how we naturally think and communicate.

## Philosophy

Prose is built on the principle that programming should be accessible and readable. Instead of cryptic symbols and abbreviated keywords, Prose uses familiar grammatical structures:

- **Phrases** (expressions) are parts of a sentence
- **Sentences** (statements) end with a period, just like in English
- **Subjects** provide scope, namespace, or represent instances
- **Nouns** (structs) represent data structures and objects
- **Verbs** (functions) represent actions and operations
- **Adjectives** represent conditions and boolean logic

## Key Features

- **Natural Language Syntax**: Write code that reads like English prose
- **Strong Type System**: Built-in types include numbers, text, and custom nouns
- **Object-Oriented**: Create custom data types with associated behaviors
- **Functional Programming**: Functions (verbs) are first-class citizens
- **Built-in Standard Library**: The `lore` scope provides essential functionality

## Example at a Glance

```prose path=null start=null
noun animal is creature {
    so head is body_part.
    so body is body_part.

    verb dance {
        it move head, and body.
    }
}

so bear is animal.
bear dance.
```

This creates a custom data type (`animal`), instantiates it (`bear`), and calls a method (`dance`) - all using natural, readable syntax.

## Getting Started

Ready to dive in? Check out the [Installation](installation.md) guide to get Prose set up on your system, then follow along with our [Hello, World!](hello-world.md) tutorial to write your first Prose program.
