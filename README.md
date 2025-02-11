# Ruby Instance Variable Modification Bug

This repository demonstrates an uncommon bug in Ruby related to modifying instance variables through getter methods.  The issue arises because the getter method returns a copy of the instance variable, not a reference. Therefore, attempting to modify the value returned by the getter method does not change the original instance variable.

## Bug Description

The provided Ruby code defines a class `MyClass` with an instance variable `@value`.  The `value` method serves as a getter.  The bug is that trying to assign a new value through the `value` method (e.g., `my_object.value = 20`) will not change the actual value of `@value`.  The assignment only modifies the local copy returned by the getter.

## Solution

To correct the behavior, you need to directly modify the instance variable using an explicit setter method or make the instance variable publicly accessible (though this is generally discouraged due to encapsulation).

## How to Run

1. Clone this repository.
2. Run the `bug.rb` file using `ruby bug.rb`. Observe the unexpected output.
3. Run the `bugSolution.rb` file to see the corrected implementation.
