# CSS Specificity Gotcha: Class Selectors Override Inherited and More Specific Styles

This repository demonstrates a subtle but important aspect of CSS specificity that can lead to unexpected style overriding.  The issue stems from the interaction of inheritance, general selectors, and the higher specificity of class selectors.

The `bug.css` file contains the problematic CSS. The `bugSolution.css` file offers a solution.

## Bug Description

A seemingly more specific CSS selector (`div p`) is overridden by a selector with a class (`special p`), even though the `div p` selector is more specific than `p` and should inherit the style from `div`. This is due to the class selector's higher specificity than the general selector.