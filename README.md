# Tailwind CSS @apply Directive Pseudo-element Inheritance Bug

This repository demonstrates a bug where Tailwind CSS's `@apply` directive doesn't correctly apply styles to pseudo-elements (::before, ::after) when used within parent classes.  The issue occurs when a class with `@apply` is applied to an element that also has pseudo-elements; the pseudo-elements may not inherit the styles from the `@apply`'d class.

## Steps to Reproduce

1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe that the button's pseudo-element styling is incorrect. It does not show `[ ` due to inheritance issue.
4. Open `bugSolution.html` for the fix.

## Solution

The solution involves avoiding the use of `@apply` for pseudo-elements or separating pseudo-element styles completely.  The example in `bugSolution.html` demonstrate this better approach. It shows more maintainable and reliable styling.