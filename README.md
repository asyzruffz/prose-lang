# Prose Programming Language

The documentation for the programming language **Prose**. It uses *mdBook* to generate the pages from Markdown files.

### [Summary](src/SUMMARY.md)

## Contribution

First install *mdBook* to start. Learn how to install it [here](https://rust-lang.github.io/mdBook/guide/installation.html).

To render the book, use the `serve` command, which will build your book and start a local webserver:

    mdbook serve --open

## Publishing

Using the `build` command in the same directory where the book.toml file is located:

    mdbook build

This will generate a directory named book which contains the HTML content of this book. You can then place this directory on any web server to host it.
