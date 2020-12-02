---
created: 2020-11-22T18:59:36+00:00
modified: 2020-11-22T23:21:29+00:00
title: Contents of a macro
---

In this post we will take a look at a basic macro to better understand its contents.

# Hello World

Hello World is the go to example when writing your first code in any language and why would here be any different.

Beginning with lines ..., the double forward slashes tell us anything that appears after them is recognised as a comment.

Lines ..., start with *using* which references code from other places so that it can be easily used in this file.

Up next is *namespace Tekla.Technology.Akit.UserScript*, *static class Script* and *public static void Run* which we don't have to go into right now other than it should remain as it is because that is known as the entry point (i.e. Tekla calls the Run method that lives in the class Script that is part of the UserScript namespace).

Then we have *MessageBox.Show("Hello World")*, which when run will show a message box with the message (you've guessed it) "Hello World". Remember the using statements which include  *System.Windows.Forms*, without that line the code would have to read *System.Windows.Forms.MessageBox.Show("Hello World)* to achieve the same result.

Now for a couple of generic C# tips.
- All code lives inside a namespace
- all code is contained within { } (or curly braces)
- all code ends with ; (semicolon)
- variables
  - string - short for textstring, contained in "" (quotation marks)
  - double - a decimal
  - int - short for integer is a whole number
  - bool - short for boolean is a true or false value.