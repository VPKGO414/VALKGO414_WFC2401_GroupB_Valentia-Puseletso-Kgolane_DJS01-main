### DJS01: Mars Climate Orbiter Challenge

# Mars Climate Orbiter Debugging

## Overview

This document outlines the debugging process for the code used in the Mars Climate Orbiter project. It highlights the changes made to improve readability, accuracy, and robustness.

## Issues

**Variable Naming:**
Variable names such as vel, acc, d, rf, and fbr are not descriptive and may not clearly convey their purpose to someone reading the code.

**Error Handling:**
There is no error handling mechanism in place to handle potential issues, such as invalid input parameters or calculation errors. This lack of error handling could lead to unexpected crashes or incorrect results.

**Function Call:**
The calcNewVel function is called before its definition, which would result in a ReferenceError. Additionally, the parameters are passed in the incorrect order (acc should be before vel).

**Calculation Errors:**
There may be potential calculation errors in the calculations for d2 and rf. The formula used for d2 (d + (vel*time)) and rf (fbr*time) may not be correct depending on the units used for the variables.

**Robustness:**
The code lacks robustness, meaning it does not check for potential issues such as invalid units of measurement or other incorrect inputs that could lead to incorrect results.

## Issues Addressed

1. **Variable Naming**: Short and unclear variable names were replaced with descriptive ones to enhance code readability.
   
2. **Error Handling**: Robust error handling was implemented to handle invalid input parameters, ensuring the program doesn't crash unexpectedly.
   
3. **Function Call**: Corrected the order of parameters in the `calcNewVel` function call to ensure it operates as intended.
   
4. **Code Organization**: The code was reorganized into logical sections with clear comments explaining each part's purpose.
   
5. **Robustness Improvements**: Input parameter validation was added to enhance the code's robustness and prevent incorrect results due to invalid inputs.

## Summary of the debugging process

The debugging process involved updating the codebase to incorporate the aforementioned improvements. The updated code now boasts descriptive variable names, robust error handling, and improved organization, making it easier to understand, maintain, and use.
