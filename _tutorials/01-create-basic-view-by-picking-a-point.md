---
name: Create basic view by picking a point
description: A simple example to demonstrate the benefit of the API.
tools: null
image: null
external_url: null
title: Create basic view by picking a point
modified: 2020-11-22T13:49:05+00:00
---

Create basic view is a command in Tekla Structures that creates a view at a level specified by the user. The problem I often have is that the level I want to create a view at isn't known, so I would have to obtain the level by some other means then input the level into the dialog to create the view.

By using a combination of a recorded macro together with some API, it is possible to create a solution that waits for the user to pick a point then use that information to create the view.

Before I continue, I should say that the API has advanced since I first wrote this code, and it's now possible to create something similar using just the API. That being said, I think this approach is better as it allows the user to apply properties before the view is created.

## Creating the macro

Begin by creating a new project from the template ...

This next portion of code is a recorded macro that opens the view properties dialog and activates the Create basic view command. 

*You can either record these steps yourself or just use the code below.*

Copy the code to the ... method

<script src="https://gist.github.com/teklanology/304cd026719d25494813b4211311e9f1.js?file=Create basic view by picking a point_1.cs"></script>

Now the API...

<script src="https://gist.github.com/teklanology/304cd026719d25494813b4211311e9f1.js?file=Create basic view by picking a point_2.cs"></script>

The complete code...

<script src="https://gist.github.com/teklanology/304cd026719d25494813b4211311e9f1.js?file=Create basic view by picking a point.cs"></script>