# CSS `calc()` Gotchas: Unit Errors and Operator Precedence

This repository demonstrates common pitfalls when using the `calc()` function in CSS and provides solutions.

## The Problem

The CSS `calc()` function is powerful, but requires careful attention to detail regarding units and operator precedence.

- **Unit Inconsistency:**  `calc()` requires units on all values. Omitting units can lead to unexpected behavior or errors. 
- **Operator Precedence:**  Incorrect use of parentheses can lead to unexpected calculations.  `calc()` follows standard mathematical operator precedence.

## Example Bug (bug.css)

The file `bug.css` demonstrates an example of a `calc()` error caused by missing units:

```css
div {
  width: calc(50% - 10); /* Error: Missing unit for 10 */
}
```

## Solution (bugSolution.css)

The corrected code in `bugSolution.css` demonstrates how to fix the unit inconsistency problem:

```css
div {
  width: calc(50% - 10px); /* Correct: Added 'px' unit */
}
```