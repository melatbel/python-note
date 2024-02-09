# 8 - Conditionals

## Conditionals

By default, statements in Python script are executed sequentially from top to bottom. If the processing logic require so, the sequential flow of execution can be altered in two way:

- Conditional execution: a block of one or more statements will be executed if a certain expression is true
- Repetitive execution: a block of one or more statements will be repetitively executed as long as a certain expression is true. In this section, we will cover *if*, *else*, *elif* statements. The comparison and logical operators we learned in previous sections will be useful here.

### If Condition

In python and other programming languages the key word *if* is used to check if a condition is true and to execute the block code. Remember the indentation after the colon.

```python
# syntax
if condition:
    this part of code runs for truthy conditions
```

**Example: 1**

```python
a = 3
if a > 0:
    print('A is a positive number')
# A is a positive number
```

As you can see in the example above, 3 is greater than 0. The condition was true and the block code was executed. However, if the condition is false, we do not see the result. In order to see the result of the falsy condition, we should have another block, which is going to be *else*.

### If Else

If condition is true the first block will be executed, if not the else condition will run.

```python
# syntax
if condition:
    this part of code runs for truthy conditions
else:
     this part of code runs for false conditions
```

- *Example: **

```python
a = 3
if a < 0:
    print('A is a negative number')
else:
    print('A is a positive number')
```

The condition above proves false, therefore the else block was executed. How about if our condition is more than two? We could use _ elif_.

### If Elif Else

In our daily life, we make decisions on daily basis. We make decisions not by checking one or two conditions but multiple conditions. As similar to life, programming is also full of conditions. We use *elif* when we have multiple conditions.

```python
# syntax
if condition:
    code
elif condition:
    code
else:
    code
```

- *Example: **

```python
a = 0
if a > 0:
    print('A is a positive number')
elif a < 0:
    print('A is a negative number')
else:
    print('A is zero')
```

### Short Hand

```python
# syntax
code if condition else code
```

- *Example: **

```python
a = 3
print('A is positive') if a > 0 else print('A is negative') # first condition met, 'A is positive' will be printed
```

### Nested Conditions

Conditions can be nested

```python
# syntax
if condition:
    code
    if condition:
    code
```

- *Example: **

```python
a = 0
if a > 0:
    if a % 2 == 0:
        print('A is a positive and even integer')
    else:
        print('A is a positive number')
elif a == 0:
    print('A is zero')
else:
    print('A is a negative number')
```

We can avoid writing nested condition by using logical operator *and*.

### If Condition and Logical Operators

```python
# syntax
if condition and condition:
    code
```

- *Example: **

```python
a = 0
if a > 0 and a % 2 == 0:
        print('A is an even and positive integer')
elif a > 0 and a % 2 !=  0:
     print('A is a positive integer')
elif a == 0:
    print('A is zero')
else:
    print('A is negative')
```

### If and Or Logical Operators

```python
# syntax
if condition or condition:
    code
```

- *Example: **

```python
user = 'James'
access_level = 3
if user == 'admin' or access_level >= 4:
        print('Access granted!')
else:
    print('Access denied!')
```