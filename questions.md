# 1. Shallow Copy of the Python List

## What is the output of the following code?

```python3
first = [1, 2, 3, 4, 5]
second = first
second.append(6)
print(first)
print(second)
```

### output
```sh
[1, 2, 3, 4, 5, 6]
[1, 2, 3, 4, 5, 6]
```

# 2. Python List Slicing Using Negative Indexing

## What is the output of the following Python code snippet?

```python3
a = [1,2,3,4,5,6,7,8,9]
print(a[-1:-5])
```

### output
```sh
[]
```

### Explanation:

The slicing syntax for the list is [a: b:c]. Here a and b are start and end indexes. The ‘c’ is the step value.

In our example, both the start and end indexes are negative values.

- a = -1 (It points to the last element in the list.)
- b = -5 (It is the index of the fifth last element in the list.)
- c = 1 (The step value is not mentioned. By default, step value is ‘1’ )

As step blue is ‘1’, we can move those values from left to right.

Actually, it first checks the start index and starts traversing to the right to find the end index. As it doesn’t find the end index it returns an empty list. Basically, if it doesn’t find a start or end index, every time it will return an empty list.

So, the output will be an empty list

# 3. Tuple and String Type
## Here is the code snippet. You have to find the type of the given three objects.

```python3
A = ("Python" , "Java")
print(type(A))
 
B = ("Python", )
print(type(B))
 
C = ("Python")
print(type(C))
```

### output
```sh
<class 'tuple'>
<class 'tuple'>
<class 'str'>
```

# 4. Differentiating List extend() Method

## What is the output of print statements 1 and 2 in the following code snippet?

```python3
listA = [1, 2, 3]
def funcA(listA):
    listA = listA * 2
    return None

funcA(listA)
print(listA) # print Statement 1
 
listB = [1, 2, 3]
def funcB(listB):
    listB=listB.extend([1, 2, 3])
    return None

funcB(listB)
print(listB) # print Statement 2
```

### output 
```sh
[1, 2, 3]
[1, 2, 3, 1, 2, 3]
```


# True or False

```sh
>>> round(1.5) == round(2.5)
```

## output 
```sh
>>> True
```

# What is the output ?
```python3
i = j = [3]
i += j
print(i, j)
```

## output
```sh
[3, 3] [3, 3]
```
## explanation
After initialization i and j refer the same [3] list object. Since list is mutable the += operation modifies the original list in place to [3,3], which is still referenced by both i and j. so `print(i,j)` will print `[3,3], [3,3]`