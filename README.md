# Silent Error in HTML: Accessing Non-Existent Element Property

This repository demonstrates a subtle and often overlooked error in HTML/JavaScript: silently accessing non-existent properties of HTML elements.  The error does not produce a JavaScript error message in the console, making it difficult to detect.

## The Problem

The `bug.html` file contains a JavaScript script that attempts to access a property (`nonExistentProperty`) that doesn't exist on the `myDiv` element.  This results in `undefined` being returned, but no error is reported.  This silent failure can lead to unexpected behavior in the application without any obvious clues.

## The Solution

The `bugSolution.html` file shows a corrected version. Before accessing properties, it explicitly checks if the property exists using a check such as the `in` operator  or by checking if the property is undefined. This prevents unexpected behavior and makes the code more robust.

## How to reproduce
1. Clone the repository
2. Open `bug.html` in a browser. Note that no error is thrown.  The alert box displays 'undefined'.
3. Open `bugSolution.html`. The alert box displays whether the property exists or not and handles it appropriately.