# Uncommon CSS Bug: :focus-visible Outline Override

This repository demonstrates a subtle bug related to the CSS `:focus-visible` pseudo-class.  The issue occurs when a more general selector unintentionally overrides the styling applied by `:focus-visible`.

## Bug Description

The `:focus-visible` pseudo-class provides a way to show focus indicators only when necessary for the user. However, if a more general selector has an `outline` style (e.g., `outline: none;`), this can inadvertently prevent the `:focus-visible` styles from applying.

## How to Reproduce

1. View the `bug.css` file.
2. Observe that the element with the class `my-element` does not show an outline when focused, even though the `:focus-visible` pseudo-class is used. 

## Solution

The solution lies in properly ordering the CSS selectors and avoiding overriding the `:focus-visible` styles.  Refer to `bugSolution.css` for the corrected code.

## Conclusion

This example highlights the importance of understanding CSS selector specificity and carefully managing style declarations to ensure that `:focus-visible` works correctly. Forcing an outline may inadvertently prevent accessibility features for some users. 