# Unexpected Dimensions with calc() in CSS

This repository demonstrates a common issue encountered when using the `calc()` function in CSS to calculate dimensions based on percentages of parent elements with undefined or relative dimensions.  The problem arises because the percentage within the `calc()` function needs a defined base value (the parent's size) to calculate correctly.

## Bug

The bug is located in `bug.css`.  The `calc()` function is used to calculate the width and height of an element based on 100% minus 20px. However, if the parent element doesn't have explicitly defined dimensions (using `px`, `em`, etc.), the calculation fails to produce the expected results.  The element's dimensions will be unpredictable.

## Solution

The solution (`bugSolution.css`) demonstrates a corrected approach.  Instead of relying solely on percentages, we set explicit dimensions for the parent element. This gives the `calc()` function a clear and reliable basis for calculating the child element's dimensions.