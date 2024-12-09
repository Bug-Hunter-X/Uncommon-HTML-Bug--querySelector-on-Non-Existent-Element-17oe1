# Uncommon HTML Bug: querySelector on Potentially Missing Element

This repository demonstrates a subtle bug that can occur in HTML when using `querySelector` on an element that might not exist or doesn't have the child element you're looking for.  This often happens when dealing with dynamically generated content or if there's a timing issue with when the `querySelector` is called relative to when the element is added to the DOM.

The `bug.html` file shows the problematic code, and `bugSolution.html` provides a solution that handles the case where the element or child element is missing.

## Reproducing the Bug

1. Open `bug.html` in a web browser.
2. Observe the console; it will show an error because `document.getElementById("myDiv").querySelector("p");`  attempts to use `querySelector` on a div that doesn't have a paragraph element.

## Solution

The solution involves adding a check to ensure the element exists before attempting to use `querySelector` on it. The improved code is in `bugSolution.html`.