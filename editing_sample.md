
### Python Traceback Overview

There are several important sections to every Python traceback. The diagram below will illustrate those sections.

{% img 'python-traceback-diagram' centered=True %}

In Python it's best to read the traceback from the bottom, moving up. The last line of the traceback is the error message line and it contains the raised exception's name (outlined in blue). Next is the error message (outlined in yellow), just above the exception name. This message usually contains information that will help you understand why the exception was raised. Moving up the traceback (outlined in green) are different functon calls, from most to least recent. Two line entries represent each function call. The first line of each call contains information like the file name, line number and module name, which all specify where you can find that section of code. The second line contains the actual code that was executed (underlined in red).

There are a few differences between the traceback's output when executing your code in the command-line and running code in the REPL. Below is the same code from the previous section executed in a `REPL` and the resulting traceback output.

\```pycon
>>> def greet( someone ):
>>>
...   print('Hello, ' +someon)
... 
>>> greet("Chad")

Traceback (most recent call last):
  File "", line 1, in 
  File "", line 2, in greet
NameError: name 'someon' is not defined
```
