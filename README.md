## Coursework – Task 1, Task 2 and Task 3
### Overview

This repository contains the solutions and analysis for:

Task 1: Enhancing Secure Data Exchange with Encoding Formats and Protocol Integration

Task 2: Computational problem analysis and complexity classification.

Task 3: Database normalization, ER modeling, and SQL implementation.

### Task 1 – Enhancing Secure Data Exchange with Encoding Formats and Protocol Integration

This project explores the role of encoding formats in secure data exchange across modern web protocols. The study evaluates Base64, Hexadecimal, and URL encoding and examines their integration with HTTPS, TLS, SMTP, REST APIs, and OAuth authentication systems.

The objective is to analyze their strengths, weaknesses, interoperability, and potential security risks, and propose improved encoding and integration strategies.

#### Introduction

Secure data exchange is essential in modern web systems including online banking, e-commerce, APIs, and email systems. Encoding formats play a key role in transforming data into safe transmission formats that are compatible with network protocols.

Encoding does not encrypt data; instead, it converts it into a different representation to ensure reliable and standardized transmission.



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
