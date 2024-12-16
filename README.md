# ConcurrentModificationException in Kotlin MutableMap

This repository demonstrates a common error in Kotlin involving `ConcurrentModificationException` when removing elements from a `MutableMap` while iterating over it.  The code in `bug.kt` shows the problematic scenario, and `bugSolution.kt` provides the corrected implementation.

## Problem

When you try to remove elements from a `MutableMap` while using its `entries` iterator, a `ConcurrentModificationException` can be thrown. This is because the iterator's internal state doesn't reflect the changes made to the map during iteration.

## Solution

The solution is to use an iterator's `remove()` method or create a copy of the keys and remove elements using that copy.