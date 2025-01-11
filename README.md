# Groovy each() Method Unexpected Behavior

This example demonstrates a common pitfall in Groovy: the `each()` method does not return a modified list.  It iterates and applies a closure to each element, but the original list remains unchanged. This often leads to unexpected null results when developers expect a transformed list to be returned.

## How to Reproduce

1. Run the `bug.groovy` script.
2. Observe that the output is `null`, not the expected transformed list `[2, 4, 6, 8, 10]`.

## Solution

Use `collect()` to create a new list containing the transformed elements.