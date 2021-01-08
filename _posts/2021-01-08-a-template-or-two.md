---
created: 2020-12-29T00:00:12+00:00
modified: 2020-12-29T23:27:05+00:00
title: A Template or Two
description: Creating macros needn't be a chore.
tags: null
---

![](../assets/a-template-or-two.png)

If you use Visual Studio to create and edit macros for Tekla Structures, then using a template is definitely the way to go. You can automatically import references and when it comes to testing your macro, Visual Studio has all the tools to debug your code.

Sharing exported templates with others can be problematic, so to remedy this I created an Visual Studio extension which contains the following types of project template:
- Script macro (what I refer to a macro without a dialog/form)
- WinForms macro (a macro with a dialog/form)

After selecting the template you want to use, you have to give your project a name. This will create a folder and .cs file with the same name. The project will then import references needed via the relevant TeklaOpenAPI NuGet package.

The structure of the .cs file allows the user to copy it from the project directory into the macros directory and run from the Components and Applications panel in Tekla Structures. Alternatively, the user can build the project to create an .exe file and run this from anywhere on the PC.

So check out the link below and please let me know what you think.
- [Project Template - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=teklanology.project-templates-01)