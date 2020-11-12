---
title: An Introduction to macros
tags: 
style: fill
color: primary
description: The writing is on the wall
---

![](https://source.unsplash.com/BofjcA9L2R0/1600x900)

## So what is a macro? 

The definition of the word macro is "a single instruction that expands automatically into a set of instructions to perform a particular task".

## The writing is on the wall

There are two methods for creating a macro for use in Tekla Structures, which are:

- recorded macro
- written macro

Recorded macros are as they sound - recorded. Tekla Structures can record your actions within the menus & dialogs and generate the associated code in a .cs file. These don't use the API directly, instead the menus & dialogs act as a middle man to interact with objects. I consider a recorded macro as static, in the sense that it can only execute actions that are recorded.

Written macros are too, as they sound. Created mostly from scratch, they interact with objects directly using the API. I prefer this method mainly because i think the dialogs are cumbersome.

In some cases a combination of the two is the only option, like when the API doesn't cater for a specific task and can only be achieved via a recorded macro.

## To WinForm or not to WinForm 

When planning your macro, you need to decide whether a form is needed. Oftentimes, a macro is simple enough that a form isn't required, and any information can be conveyed to the user via fhe status bar in Tekla Structures.

## Do you LinkedIn?

In addition to my other connected accounts, I have now created a [LinkedIn page](https://www.linkedin.com/company/teklanology), so feel free to say hi.
