# Installation

This guide will walk you through installing the Prose programming language on your system.

## Prerequisites

Before installing Prose, make sure you have:

- A modern operating system (Windows 10+, macOS 10.15+, or Linux)
- At least 100MB of free disk space
- Internet connection for downloading packages

## Installation Methods

Prose has its own project manager cum package manager called **stitch**. To start coding in Prose, you need to install stitch.

### Method 1: Pre-built Binaries (Recommended)

1. **Download the latest release** from the official stitch repository:
   - Visit [https://github.com/asyzruffz/stitch/releases](https://github.com/asyzruffz/stitch/releases)
   - Download the appropriate binary for your operating system

2. **Extract and install**:
   - **Windows**: Extract the `.zip` file and add the `stitch.exe` to your PATH
   - **macOS**: Extract the `.tar.gz` file and move `stitch` to `/usr/local/bin`
   - **Linux**: Extract the `.tar.gz` file and move `stitch` to `/usr/local/bin`

3. **Verify installation**:
   ```bash
   stitch --version
   ```

### Method 2: Build from Source

1. **Install build dependencies**:
   - Rust toolchain (1.60.0 or later)
   - Git

2. **Clone the repository**:
   ```bash
   git clone https://github.com/asyzruffz/stitch.git
   cd stitch
   ```

3. **Build and install**:
   ```bash
   cargo build --release
   cargo install --path .
   ```

4. **Verify installation**:
   ```bash
   stitch --version
   ```

## Setting up your Development Environment

### Text Editors and IDEs

While Prose can be written in any text editor, these provide enhanced support:

- **VS Code**: Install the "Prose" extension for syntax highlighting
- **Vim/Neovim**: Use the `prose.vim` syntax file
- **Emacs**: Use `prose-mode` for syntax highlighting
- **Sublime Text**: Install the Prose package via Package Control

### File Extension

Prose source files use the `.prs` extension:

```
myprogram.prs
```

## Running Your First Program

Once installed, you can run Prose programs using:

```bash
stitch run myprogram.prs
```

Or compile to an executable:

```bash
stitch build myprogram.prs
./myprogram
```

## Troubleshooting

### Common Issues

**"stitch: command not found"**
- Make sure the stitch binary is in your system's PATH
- Try running with the full path to the binary

**Permission denied errors**
- On Unix systems, make sure the binary has execute permissions:
  ```bash
  chmod +x stitch
  ```

**Build errors when compiling from source**
- Ensure you have the latest Rust toolchain installed
- Try updating your dependencies:
  ```bash
  cargo update
  ```

## Next Steps

Now that stitch is installed, you're ready to write your first Prose program! Continue to the [Hello, World!](hello-world.md) tutorial to get started.
