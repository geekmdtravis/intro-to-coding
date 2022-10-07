# [Intro to Coding](https://github.com/geekmdtravis/intro-to-coding)

[Travis Nesbit, MD](https://www.linkedin.com/in/travis-nesbit-md-953b70a4/) ([geekmdtravis](https://github.com/geekmdtravis/))

## TL;DR

- Find an online course that you like (I like [Udemy](https://www.udemy.com/)).
- Ensure you're using version control
- Ensure you're writing unit tests
- Ensure you're using your debugger
- Practice. Practice. Practice.
- Always ask _why_.

## Goals

The focus of this introductory session is to give each participate an understanding of:

- Do I need a computer science degree to become a high-earning software engineer?
- Basic concepts of computer programming.
- Commonly used introductory programming languages.
- My choice of introductory programming languages.
- Major tools commonly used in computer programming and **why** they're used.
- Where and how to begin learning to program **without** a complex development environment.

## Do I need a computer science degree to become a high-earning software engineer?

_Absolutely not._ I do not consider myself to be an expert in the area of hiring, but my personal experience and shared anecdotes the degree helps you getting intro jobs when you lack a portfolio of work. However, once you have a portfolio of work that demonstrates your capability the meritocratic culture in software engineering tends to take over.

### What is a portfolio of work?

It's really anything that displays your skill. If you've had jobs previously, that work experience will be much of your portfolio. If you're self-taught, you'll want to put your projects on [GitHub](https://github.com) (or similar) and if possible find ways to contribute to open source tools (earlier said than done).

### How can I contribute to open source projects?

This is a bit easier said than done, and you're likely a thinking a few steps too far ahead. ^\_^ Open source projects often have a quite high standard for code contributions. But, there are many ways to contribute. I will defer this entire conversation to the [Open Source Guide](https://opensource.guide/how-to-contribute/).

## Basic concepts of computer programming

We're going to stay high-level here and avoid the dirty details of how a computer works. When you write a computer program using a modern computer lanugage, in short you use storage _containers_ that we generally call _variables_ to keep track of data. In reality, it's often more of the storage of an address to the data, but that's a bit too much detail for this introductory session. We then use a number of logic and flow control operators to manipulate the data contained in variables.

### Common Data Types

- `string` - a sequence of characters that are generally intended to be represented as some form of text. (under the hood they're simply numbers that we've arbitrarily chosen to treat differently).
- `integer` - a whole number.
- `float` - a number with a decimal point.
- `boolean` - a value that is either `true` or `false` (under the hood it's generally also a `0` or `1`).

### Commonly used Logical Operators

- `==` - Equal to
- `!=` - Not equal to
- `>` - Greater than
- `<` - Less than
- `>=` - Greater than or equal to
- `<=` - Less than or equal to
- `&&` - And
- `||` - Or

### Commonly used Control Flow Operations

- `if` - If the condition is true, execute the code block.
- `else` - If the condition is false, execute the code block.
- `else if` - If the condition is false, execute the code block.
- `switch` - If the condition is true, execute the code block.
- `while` - While the condition is true, execute the code block.
- `for` - For the number of times specified, execute the code block.
- `for each` - For each item in the collection, execute the code block.

### Common Ways of Grouping Code

- `function` - Functions are used to abstract code blocks into smaller chunks.
- `{}` - Curly braces are used to group code blocks into a certain _scope_.
- `class` - Classes are used effectively like templates which group related data and data operations; from these templates we can make _instances_ (or actualy data chunks that live in your computers memory) that are unique and whose data can be handled in isolation.

### Common Data Structures

- `list` or `array` - A collection of data that is ordered -- each item has a position with an identifying number starting at `0` -- and can be accessed by that position.
- `map` - A collection of data whose values can be accessed quickly and directly by their _key_ and which does not necessarily have order.

_An Example Program in TypeScript_

```typescript
let myName: string = "Travis Nesbit";
let yourName: string = "John Rambo";

let ourNames = [myName, yourName];

ourNames.forEach((name) => {
  if (name === "John Rambo") {
    console.log("You don't need to know my name.");
  } else {
    console.log(`Hi, my name is${name}`);
  }
});
```

In the above code we created two variables, `myName` and `yourName`, and assigned them a value of type `string`. We then created a new variable, `ourNames`, and assigned it a value of type `list` or `array` which contains the values of `myName` and `yourName`. We then used a `forEach` loop to iterate over each item in the `ourNames` list and print a message to the console.

## Commonly used introductory programming languages

I won't get into details, but the following are programming languages commonly used to teach introductory programming concepts. This is because the programs which are responsible for taking the text you write as code and converting it into a series of computer instructions are for more forgiving and do not require that you do more complicated tasks such as manually managing the data you instruct the program put inside of your computers memory.

These languages are all widely used, well documented, and have a large community of developers who are willing to help you learn. The major difference between them from the perspective of a beginner will be accessibility (how easy is it to start programming) and whether or not the code is `typed`. Some languages do not require the variable you work with has a declared data type, and some do.

- [JavaScript](https://www.javascript.com/)
- [Python](https://www.python.org/)
- [Java](https://www.java.com/en/)
- [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
- [TypeScript](https://www.typescriptlang.org/)

## My choice of introductory programming languages

I have a strong prefernce for typed languages. They both make you consider what you're doing and prevent many errors. For that reason, I think TypeScript is the best choice for a beginner. It's a typed version of JavaScript, which is the most popular programming language in the world. It's also a language that is used in the majority of web development, which is a great place to start. The next best choice would be Python, which is a very popular language that is used in a wide variety of applications and has support for _type annotations_ (that is, you can declare the type of a variable, but it's not required).

- [TypeScript](https://www.typescriptlang.org)
- [Python](https://www.python.org/)

Eventually, I think every programmer should also experience some lower level programming languages like _C_ and _Assembly_ so that you can gain a better understanding of how computers work. But, that's a bit too much for an introductory session.

## Major tools commonly used in computer programming and why they're used

### Text Editor

A text editor is a program that supports you as you to write code. You can technically write code in any text editor so long as it's storing the data as raw text (think Windows Notepad). But, in 2022 that's unneccesarily tedious since text editors for software development have tools that help you write code more efficiently.

### Integrated Development Environment (IDE)

An IDE is a program that combines a text editor with other tools that are commonly used in software development. It's a very powerful tool that can help you write code more efficiently, but I personally advocate against their use in the beginning because they're (a) bloated, and (b) can negatively impact your learning as they can hide the details of what's happening under the hood.

### Code Debugger

The debugger is a tool that allows you to step through your code and see what's happening at each step in terms of what data is inside what variable, and how your flow control and logical statements are operating. It's a very powerful tool that can help you understand what's happening in your code when behavior isn't what you expect.

### Unit Testing Framework

A unit testing framework is a tool (generally written in the same language that you're using and made available as a library) that allows you to write tests that can be run against your code to verify that it's working as expected. It's a very powerful tool that can help you write code that is more reliable and less prone to errors.

### Package Manager

A package manager is a tool that allows you to download and install libraries that other developers have written and made available for you to use in your own code. It's a very powerful tool that can help you write code that is more reliable and less prone to errors since other people have already solved many of the problems you're trying to solve.

### Version Control

Version control is a system that allows you to keep track of changes to your code. It's a very powerful tool that allows you to easily revert to previous versions of your code, collaborate with others, and keep track of changes to your code.

### Terminal Emulator

A terminal emulator is a program that allows you to interact with your computer using a text based interface. It's a very powerful tool that allows you to do things like navigate your file system, run programs, and install software. In Windows it's called the _Command Prompt_ or _PowerShell_ and in macOS and other POSIX compliant operating systems it's referred to as the _Terminal_. Of note, you can install different terminal emulators in your computer than what comes with them by default.

### Examples of the above tools

- [Visual Studio Code](https://code.visualstudio.com/) - A free text editor that is used to write code. It's free, open source, and has a large community of developers who are willing to help you learn. A _debugger_ will be built into this.
- [JetBrains WebStorm](https://www.jetbrains.com/webstorm/) - A paid IDE that is very powerful and has a lot of features. A _debugger_ will be built into this.
- [Anaconda](https://www.anaconda.com/products/distribution) - A free package manager that is used to install Python libraries.
- [NPM](https://www.npmjs.com/) - A free package manager that is used to install JavaScript libraries.
- [Git Bash](https://git-scm.com/downloads) - A UNIX-like terminal emulator that can be run on Windows as an alternative to the default Command Prompt or PowerShell. It's made available when you install _Git_.
- [Git](https://git-scm.com/) - A version control system that is used to track changes to your code and to collaborate with other developers.
- [GitHub](https://github.com) - A website that allows you to host your code and collaborate with other developers. It interacts seamlessly with the version control system Git.

## Where and how to begin learning to program without a complex development environment

- [Solo Learn](https://www.sololearn.com/compiler-playground/cOAXyhEmN1f7) - A free website that allows you to write code in your browser and run it. It's a great place to start learning to program.
- [PlayCode.io](https://playcode.io/typescript) - A free website that allows you to write code in your browser and run it. It's a great place to start learning to program.
- [CodePen](https://codepen.io/) - A free website that allows you to write code in your browser and run it. It's a great place to start learning to program.

- [YouTube](https://www.youtube.com/) - You know what this one is. Ha, ha.
- [Stack Overflow](https://stackoverflow.com/) - A website where you can ask questions about programming and get answers from other developers.
- [Udemy](https://www.udemy.com/) - A website where you can take online courses to learn how to program. It's inexpensive and has a large selection of courses. **I strongly recommend this resource**.
