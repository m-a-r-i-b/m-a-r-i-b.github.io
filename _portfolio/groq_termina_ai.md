---
title: "AI-Powered CLI Assistant"
excerpt: "Python, LLMs, bash, Groq, PyPi"
header:
  teaser: "assets/images/groq-terminal-ai.jpg"
sidebar:
  - title: "Role"
    text: "Creator & Developer"
  - title: "Responsibilities"
    text: "Full Development"
tags:
  - Python
  - CLI
  - AI
  - LLM
  - Open Source
---

## The Problem

As developers, we frequently find ourselves needing to perform complex terminal operations - from batch renaming files to searching through directories with specific patterns. While these tasks are perfectly doable with command-line tools, remembering the exact syntax and flags can be challenging and time-consuming.The source code can be found in this [repository](https://github.com/m-a-r-i-b/groq-terminal-ai).

The traditional workflow often involves:
1. Leaving the terminal
2. Opening a browser
3. Asking ChatGPT or searching Stack Overflow
4. Copying the command
5. Returning to terminal
6. Executing the command

This context-switching is inefficient and breaks the flow of work.

## The Solution

I created **groq-terminal-ai**, a CLI tool that brings the power of Large Language Models directly to your terminal. It converts natural language instructions into terminal commands instantly, without ever leaving your command line interface.

### Key Features

- **AI-Powered Command Generation**: Utilizes Groq's advanced language models to interpret natural language and generate accurate commands
- **Cross-Platform Support**: Works seamlessly on Linux, macOS, and Windows
- **Smart Caching**: Implements efficient command caching to quickly retrieve previously generated commands
- **Context-Aware**: Maintains command history for more accurate suggestions
- **Model Flexibility**: Supports multiple Groq LLM models including:
  - llama3-8b-8192
  - gemma2-9b-it
  - llama3-70b-8192
  - mixtral-8x7b-32768
  - and more

## Implementation

The tool is built in Python and is available as a PyPI package. It interfaces with Groq's API to access their state-of-the-art language models, known for their exceptional speed and accuracy.

### Installation
```bash
pip install groq-terminal-ai
```

### Usage Example
```bash
# Set your API key
ai --groq-api-key <your-api-key>

# Generate commands using natural language
ai list all png files in the current directory
```

## Impact & Results

The tool significantly streamlines terminal operations by:
- Eliminating context switching
- Reducing time spent searching for command syntax
- Providing consistent command generation across different operating systems
- Maintaining command history for repeated tasks

## Links

- [GitHub Repository](https://github.com/m-a-r-i-b/groq-terminal-ai)
- [PyPI Package](https://pypi.org/project/groq-terminal-ai/)

