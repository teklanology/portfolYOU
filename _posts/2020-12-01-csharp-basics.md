---
title: C# basics
description: Understanding the basics
tags: null
---

## Hello World!

Programming languages often have their own version of the *Hello World!* program that serves as an introduction to the basics of the language.

By modifying C#'s version slightly, the code below will not only look familiar to those who record and edit macros, it will also run in Tekla Structures.

<pre>
using System.Windows.Forms;

namespace Tekla.Technology.Akit.UserScript
{
    // A version of the classic "Hello, World! program
    static class Script
    {
        public static void Run(Tekla.Technology.Akit.IScript RunMe)
        {
            MessageBox.Show("Hello, World!");
        }
    }
}
</pre>

Now let's examine the code line by line.

## The *Using* Keyword 

By using the `using` keyword, the first line imports all types within the `System.Windows.Forms` namespace. For example, the `MessageBox` class used later in the source code is defined in the `System.Windows.Forms` namespace, meaning it can be used without writing the full name of the type. A program can include multiple lines of `using` statements, for example:

<pre>
using System;
using System.Windows.Forms;
</pre>

## Namespaces

Namespaces are heavily used in C# programming in two ways. First, .NET uses namespaces to organize its many classes, and secondly, declaring your own namespaces can help you control the scope of class and method names in larger programming projects. Use the `namespace` keyword to declare a namespace, as in the following example:

<pre>
namespace Tekla.Technology.Akit.UserScript
{
    ...
}
</pre>

## Comments

Comments are used for explaining code, which the compilers ignore when compiling. Single-line comments are indicated by the `//` symbol.

<pre>// A version of the classic "Hello, World!" program</pre>

Whereas multi-line comments start with `/*` and terminate with the `*/` as shown below:

<pre>
/* This program demonstrates
   The basic syntax of C# programming 
   Language */
</pre>


## Classes

Everything that follows between the pair of curly braces describes that class and demarcate the boundaries of a code block. Curly braces are used to group statements, which are commonly grouped into methods (functions), methods into classes, and classes into namespaces. In example below, they are marking the start and end of the `Script` class.

<pre>
static class Script
{
    ...
}
</pre>

## Methods

The line below declares the class member method called `Run`, where the program begins execution.
 - The `public` keyword tells the compiler that the method can be called from anywhere by any class. 
 - The `static` keyword makes the method accessible without an instance of `Script`. 
 - The `void` keyword declares that `Run` has no return value.

<pre>public static void Run(Tekla.Technology.Akit.IScript RunMe)</pre>

The line below displays the message box. The program calls the `MessageBox` method `Show`, which displays a message box with the contents "Hello, World!".

<pre>MessageBox.Show("Hello, World!");</pre>