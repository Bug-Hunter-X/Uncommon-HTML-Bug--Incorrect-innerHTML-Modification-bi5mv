# Uncommon HTML Bug: Incorrect innerHTML Modification

This repository demonstrates a subtle bug in HTML related to modifying the `innerHTML` property of an element before the element is fully parsed and added to the DOM tree.  The bug is not immediately obvious to developers not fully understanding the browser's DOM rendering process.

## Bug Description

The primary issue is that the code attempts to manipulate the `innerHTML` property of a div element before the browser has finished loading the entire HTML document.  This often results in no change, or a JavaScript error.

## Solution

The solution involves using the `DOMContentLoaded` event listener, which waits for the entire HTML document to be loaded and parsed before executing the code that manipulates the `innerHTML` property of the div element.

## How to reproduce the bug

1. Open `bug.html` in a web browser.
2. Observe that the text within the div element does not change as expected.