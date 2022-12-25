---
layout: post
title:  "Singleton design pattern in Python"
date:   2022-10-23 11:17:05 +0700
categories: Python, design-pattern, creational
---

## What?
Singleton pattern:
- Ensure that a class has just a single instance
- Provide global access point to that instance

## How?
- Make the default constructure private, to prevent other objects from using the new operator
- Create a static creation method that acts as a constructor and this method calls the private constructor to create an object and saves it in a static field. All following calls to this method return the cached object
