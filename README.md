# LeetCode 1111 - Maximum Nesting Depth of Two Valid Parentheses Strings

## Problem

Given a valid parentheses string `seq`, split it into two valid parentheses strings `A` and `B` such that:

A + B = seq

Return an array where:

- `0` means the character belongs to `A`
- `1` means the character belongs to `B`

The goal is to minimize the maximum nesting depth between the two strings.

---

## Approach

The main idea is to alternate nested levels between the two groups.

We maintain a variable:

depth = current nesting depth

For an opening parenthesis `(`:

```java
answer[i] = depth % 2;
depth++;
