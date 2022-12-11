---
layout: post
title:  "Inside hashes in PostgreSQL"
date:   2022-10-23 11:17:05 +0700
categories: Python, programming
---

This note is just for my personal reference. The original video: [https://www.coursera.org/learn/intermediate-postgresql/lecture/G9upZ/inside-hashes](https://www.coursera.org/learn/intermediate-postgresql/lecture/G9upZ/inside-hashes)

### What is a hash function?
Link: [https://en.wikipedia.org/wiki/Hash_function](https://en.wikipedia.org/wiki/Hash_function)
- A hash function is any function that can be used to map data of arbitrary size to **fixed-size** values. 
- The values returned by a hash function are called **hash values**, **hash codes**, **digests**, or simply **hashes**. 
- The values are usually used to index a fixed-size table called a **hash table**. 
- Use of a hash function to index a hash table is called **hashing**

### Uses of Hashes
- Python dictionaries
- Database indexes

### Good Hash Functions
- **Deterministic**: Must get the same output for the same input
- **Uniform Distribution**: Should have an equal chance of generating any value with the range of its outputs
- **Sensitive**: Any change in input should provide a change in output
- **One-way**: You should not be able to derive the input from the output

