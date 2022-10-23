---
layout: post
title:  "How to make your code Pythonic"
date:   2022-10-23 11:17:05 +0700
categories: Python, programming
---
To make your Python code Pythonic, you should follow 2 coding style guidelines: PEP 8 and PEP 20. Let's dive into them now
## PEP 8
- PEP 8 is about guidelines for
  - Code layout
  - Whitespace
  - Naming conventions
  - Other similar style topics
- Take the following example, a file `pythonic.py`
{% highlight python %}
import math, os

def printer(name,message):
  print(f"You have a new message from {name}")
  print(f"{message}")

printer(name="Peter", message='Hi')
{% endhighlight %}
To check PEP8, you can use `pycodestyle` tool in command line
{% highlight %}
pycodestyle pythonic.py

pythonic.py:1:12: E401 multiple imports on one line
pythonic.py:3:1: E302 expected 2 blank lines, found 1
pythonic.py:3:17: E231 missing whitespace after ','
{% endhighlight %}

## PEP 20
