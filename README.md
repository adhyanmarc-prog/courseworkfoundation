# Coursework – Task 1, Task 2 and Task 3
# Overview

This repository contains the solutions and analysis for:

Task 1: Enhancing Secure Data Exchange with Encoding Formats and Protocol Integration

Task 2: Computational problem analysis and complexity classification.

Task 3: Database normalization, ER modeling, and SQL implementation.

## Task 1 – Enhancing Secure Data Exchange with Encoding Formats and Protocol Integration

This project explores the role of encoding formats in secure data exchange across modern web protocols. The study evaluates Base64, Hexadecimal, and URL encoding and examines their integration with HTTPS, TLS, SMTP, REST APIs, and OAuth authentication systems.

The objective is to analyze their strengths, weaknesses, interoperability, and potential security risks, and propose improved encoding and integration strategies.

### Introduction

Secure data exchange is essential in modern web systems including online banking, e-commerce, APIs, and email systems. Encoding formats play a key role in transforming data into safe transmission formats that are compatible with network protocols.

Encoding does not encrypt data; instead, it converts it into a different representation to ensure reliable and standardized transmission.

#### Base64 Encoding

Base64 converts binary data into ASCII text format.

Strengths:

Safe for HTTP transmission

Required for email attachments (MIME)

Used in OAuth tokens and API authentication

Prevents data corruption in text-based protocols

Weaknesses:

Increases data size by ~33%

Not secure by itself

Easily reversible

#### Hex encoding converts binary data into base-16 representation.

Strengths:

Easy debugging

Used in cryptographic hashes (SHA-256, MD5)

Human-readable representation

Weaknesses:

Doubles data size

No confidentiality protection

#### URL Encoding

URL encoding ensures safe transmission of special characters in URLs.

Strengths:

Prevents malformed URLs

Essential for REST APIs

Protects against injection in query parameters

Weaknesses:

Can be abused for obfuscation attacks

Double encoding attacks possible

### Encoding in Secure HTTP Transmission

When a client sends data over HTTPS:

Data may be URL encoded (form submission)

JSON payload may contain Base64-encoded binary data

TLS encrypts the entire transmission

Encoding ensures data structure integrity.
TLS ensures confidentiality and integrity.

Encoding ≠ Encryption.

### Role in TLS and HTTPS

TLS provides:

Confidentiality

Integrity

Authentication

Encoding ensures:

Protocol compatibility

Safe formatting

Reliable payload transmission

Example:

OAuth tokens are Base64 encoded before transmission

TLS encrypts them during transit

### Role in SMTP (Email Transmission)

Email attachments are encoded in Base64 before being sent via SMTP because SMTP supports only text-based transmission.

Flow:

File → Base64 encoding

Encoded data → SMTP transmission

Receiver decodes Base64

TLS secures the channel

Without encoding, binary files would corrupt during transfer.

### Risks of Encoding-Based Obfuscation

Attackers misuse encoding to:

Hide malicious payloads

Bypass filters

Perform double encoding attacks

Hide SQL injection attempts

Example:
Malicious payload encoded in Base64 to evade detection.

Therefore:
Security systems must decode and inspect payloads before validation.

### Interoperability with Modern Web Protocols

Encoding formats integrate with:

REST APIs (JSON payloads)

OAuth authentication (Base64 tokens)

HTTPS/TLS encryption

SMTP email systems

Web forms and query parameters

Encoding ensures cross-platform compatibility between systems.

### Proposed Improvements

To enhance secure data exchange:

Always combine encoding with TLS encryption

Implement strict input validation after decoding

Detect double encoding attacks

Use Content Security Policy (CSP)

Use secure token formats (JWT with signature validation)

Apply rate limiting to prevent encoded attack flooding

### Conclusion

Encoding formats such as Base64, Hex, and URL encoding are essential for secure and efficient data transmission. However, encoding alone does not provide security.

When integrated properly with HTTPS, TLS, SMTP, and OAuth mechanisms, encoding enhances reliability and interoperability while encryption ensures confidentiality.

Proper validation and decoding analysis are necessary to prevent encoding-based obfuscation attacks.


## Task 2 – Computational Complexity Analysis
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
