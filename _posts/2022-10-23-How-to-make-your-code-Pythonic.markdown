---
layout: post
title:  "How to make your code Pythonic?"
date:   2022-10-23 11:17:05 +0700
categories: Python, programming
---
To make your Python code Pythonic, you should follow 2 coding style guidelines: PEP 8 and PEP 20. Let's dive into them now!
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

  - To check PEP8, you can use `pycodestyle` tool in command line
{% highlight bash %}
pycodestyle pythonic.py

pythonic.py:1:12: E401 multiple imports on one line
pythonic.py:3:1: E302 expected 2 blank lines, found 1
pythonic.py:3:17: E231 missing whitespace after ','
{% endhighlight %}

  - To do PEP8 code automatic reformatting, you can use autopep8
{% highlight bash %}
autopep8 --in-place pythonic.py
{% endhighlight %}

## PEP 20
{% highlight bash %}
➜  ~ python3
Python 3.7.13 (default, Oct 11 2022, 09:28:42)
[Clang 14.0.0 (clang-1400.0.29.102)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import this
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
>>>
{% endhighlight %}

> Beautiful is better than ugly

> Explicit is better than implicit
{% highlight python %}
from math import sin

def sin():
  print("Your sin function logic")
{% endhighlight %}

> Simple is better than complex

> Complex is better than complicated

> Flat is better than nested

> Sparse is better than dense

> Readability counts

{% highlight python %}
# Low readability code
sn = ["Bob", "Jack", "Harry"]

for n in sn:
  print(n)
{% endhighlight %}

{% highlight python %}
# Hide readability code
student_names = ["Bob", "Jack", "Harry"]

for name in student_names:
  print(name)
{% endhighlight %}

> Special cases aren’t special enough to break the rules
> Although practicality beats purity

> Errors should never pass silently
> Unless explicitly silenced

- Error is passed siliently
{% highlight python %}
a = 1
b = 0

try:
  c = a / b
except:
  pass
{% endhighlight %}

- Error is handled and logged
{% highlight python %}
a = 1
b = 0

try:
  c = a / b
except ZeroDivisionError:
  print("Can not divide by zero!")
{% endhighlight %}

> In the face of ambiguity, refuse the temptation to guess

> There should be one, and preferably only one way to do it
> Although that way may not be obvious at first unless you’re Dutch

{% highlight python %}
# Using the % operator
programming_language = "Python"
print("The Zen of %s" % programming_language)

# Using the .format() method
print("The Zen of {}".format(programming_language))

# Using f-string
print(f"The Zen of {programming_language}")
{% endhighlight %}

> Now is better than never
> Although never is often better than right now

> If the implementation is hard to explain, it’s a bad idea
> If the implementation is easy to explain, it may be a good idea

> Namespaces are one honking great idea -- let’s do more of those!
{% highlight python %}
def chase():
  # Good namespacing
  import cartoon.models.cat as cat
  import cartoon.models.dog as dog
  
  dog.chase(cat)
  cat.chase(mouse)
{% endhighlight %}

There should be 20 guidelines for PEP 20, but you can see that there are just 19 of them, the 20th guideline is up to you to define!
