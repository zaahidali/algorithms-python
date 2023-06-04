# Bubble Sort and Searching Algorithms

This repository contains Python implementations of the Bubble Sort algorithm and various searching algorithms, including Linear Search and Binary Search.

## Bubble Sort Algorithm

The Bubble Sort algorithm is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The algorithm continues until the list is sorted.

### Usage

Here is an example usage of the Bubble Sort algorithm:

```python
l1 = [4,2,1,6,7,5]

lsorted=True
while lsorted==True:
    lsorted=False
    for i in range(len(l1)-1):
        if l1[i] > l1[i+1]:
            l1[i],l1[i+1] = l1[i+1],l1[i]
            lsorted=True
print(l1)
```

Output:
```
[1, 2, 4, 5, 6, 7]
```

## Linear Search Algorithm

The Linear Search algorithm is a simple searching algorithm that sequentially checks each element in a list until a match is found or the end of the list is reached.

### Usage

Here is an example usage of the Linear Search algorithm:

```python
l2 = [5,4,7,8,9,3,2,1,11,14,198,412,25,6]
sno = 6
element = -1
for i in range(len(l2)):
    if l2[i] == sno:
        element = l2[i]
        print("The element "+str(l2[i])+": found at index: "+str(i))
        break
if element== -1:
    print("The element does not exist")
```

Output:
```
The element 6: found at index: 13
```

## Binary Search Algorithm

The Binary Search algorithm is a more efficient searching algorithm for sorted lists. It works by repeatedly dividing the search interval in half until the target value is found or the interval is empty.

### Usage

Here is an example usage of the Binary Search algorithm:

```python
l = [2, 3, 5, 8, 11, 12, 18]
search_for = 11
slice_start = 0
slice_end = len(l) - 1
found = False

while slice_start <= slice_end and not found:
    location = (slice_start + slice_end) // 2
    if l[location] == search_for:
        found = True
        print("The value found at index : "+str(location))
    else:
        if search_for < l[location]:
            slice_end = location - 1
        else:
            slice_start = location + 1
print(found)
print(location)
```

Output:
```
The value found at index : 4
True
4
```

Feel free to explore and modify the code to understand the algorithms better.

## License

This repository is licensed under the [MIT License](LICENSE).
