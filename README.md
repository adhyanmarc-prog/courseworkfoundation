## Coursework – Task 1 and Task 3
### Overview

This repository contains the solutions and analysis for:

Task 1: Enhancing Secure Data Exchange with Encoding Formats and Protocol Integration

Task 2: Computational problem analysis and complexity classification.

Task 3: Database normalization, ER modeling, and SQL implementation.



### Task 2 – Computational Complexity Analysis
 Problem Description

A teacher must arrange students in a single row of seats before an examination with the following constraints:

1. Friends cannot sit next to each other.

2. Students from the same city cannot sit next to each other.

3. Every student must be seated exactly once.

The problem is to determine whether a valid seating arrangement exists that satisfies all constraints.

### Complexity Classification

This problem is classified as NP (Non-deterministic Polynomial time).

#### Reason:

The number of possible seating arrangements for n students is:

n! (factorial growth)

To verify whether one arrangement satisfies the constraints takes polynomial time O(n).

However, generating all possible permutations requires factorial time.

#### Therefore:

Verification → Polynomial time

Search space → Exponential growth

Overall → NP problem
