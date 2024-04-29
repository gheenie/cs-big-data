### BDA Seminar 1 - Part 1 & 2

**Complete the following exercises on computational complexity.**

1. Study the following script. This program implements a `linear_search(arr, x)` function that returns element `x`'s index in the list `arr`. If `x` is not found, it returns `-1`.

```python
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1
```

2. Now, let's put your understanding to the test. Can you determine the time complexity of the following script? Take a moment to think about it.

```Py
if __name__ == "__main__":
  data = [10,20,30,40,50,50,60,80,90,100]
  result = linear_search(data,40)
  print(result)
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

3. What is the space complexity of the above script?

| Provide your answer here. |
| ------------------------- |
| ?                         |

4. Is this a computationally or data-intensive task?

| Provide your answer here. |
| ------------------------- |
| Computationally           |

> [!TIP]
>
> Start using the conditional statement when creating programs. `if __name__ == "__main__"`
>
> This block often includes test code, demonstration code, or main application logic that you don't want to run if the file is imported as a module in another script.

5. What is the time complexity of the following code?

```python
if __name__ == "__main__":
  data = [10,20,30,40,50,50,60,80,90,100]
  print(data[-1])
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

6. What is the time complexity of the following code?

```python
def get_it(arr):
    for i in arr:
      return i

if __name__ == "__main__":
  data = [10,20,30,40,50,50,60,80,90,100]
  print(get_it(data))
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

7. What is the time complexity of the following code?

```python
ef sum_elements(arr):
    total = 0
    for num in arr:
        total += num
    return total

if __name__ == "__main__":
  data = [10,20,30,40,50,50,60,80,90,100]
  print(sum_elements(data))
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

8. Is this a computationally or data-intensive task?

| Provide your answer here. |
| ------------------------- |
| ?                         |

9. What is the time complexity of the following code?

```python
def count_characters(filename):
  count=0
  with open(filename, 'r') as file:
    for char in file:
      count+=1
            
  return count

if __name__ == "__main__":
  filename = 'file1.txt'
  try:
      counts = count_characters(filename)
      print("Letter counts:", counts)
  except FileNotFoundError:
      print("File not found")
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

> [!IMPORTANT]
>
> ❗To execute the script, ensure that the `file1.txt` is in the same directory as your Python script.

10. What is the space complexity of the above code?

| Provide your answer here. |
| ------------------------- |
| ?                         |

11. Is this a computationally or data-intensive task?

| Provide your answer here. |
| ------------------------- |
| ?                         |

12. Compare the following scripts; which one do you prefer and why?

    Pick one of the following options:

    \* `reverse1` is better

    \* `reverse2` is better

    \* Both are the same

| Provide your answer here. |
| ------------------------- |
| ?                         |

12. What are the time and space complexities for reverse1 and reverse2?

| Provide your answer here. |
| ------------------------- |
| `reverse1`: ?             |
| `reverse2`: ?             |

12. What is the time complexity of the following code?

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

if __name__ == "__main__":
  data = [64, 34, 25, 12, 22, 11, 90]
  print(bubble_sort(data))
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

13. What is the space complexity of the previous script?

| Provide your answer here. |
| ------------------------- |
| ?                         |

14. Examine the next code.

```python
 def bubble_sort_count1(arr):
    n = len(arr)
    count_n=0
    for i in range(n):
        for j in range(0, n-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
            count_n+=1
    return count_n

if __name__ == "__main__":
  data = [10, 9, 88, 7, 62, 5, 43]
  print(bubble_sort_count1(data))
```

15. What is the purpose of this script?

| Provide your answer here. |
| ------------------------- |
| ?                         |

16. What is the time complexity of this script?

| Provide your answer here. |
| ------------------------- |
| ?                         |

17. Analyze the Provided Code.

```python
 def bubble_sort_count2(arr):
    n = len(arr)
    count_n=0
    for i in range(n):
        for j in range(0, n-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                count_n+=1
    return count_n

if __name__ == "__main__":
  data = [10, 9, 88, 7, 62, 5, 43]
  print(bubble_sort_count2(data))
```

18. What is the purpose of the script? 

| Provide your answer here. |
| ------------------------- |
| ?                         |

19. Why does it output 12?

| Provide your answer here. |
| ------------------------- |
| ?                         |

20. What is the purpose of the script?

> [!TIP]
>
> Examine the code.

```python
 def bubble_sort_count3(arr):
    n = len(arr)
    count_n=0
    for i in range(n):
        for j in range(0, n-1-i):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
            count_n+=1
    return count_n

if __name__ == "__main__":
  data = [10, 9, 88, 7, 62, 5, 43]
  print(bubble_sort_count3(data))
```

21. Why does it output 21?

| Provide your answer here. |
| ------------------------- |
| ?                         |

22. What is the time complexity of this script?

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = left + (right - left) // 2 # // means integer division (5//2)=2 :)
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

if __name__ == "__main__":
  data = [10, 19, 28, 32, 45, 55, 66]
  target = 28
  print(binary_search(data, target))
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

23. The following script generates all the possible permutations of a given list. Without running the script, can you defien the time complexity of this script?

```python
from itertools import permutations

def all_permutations(elements):
    return list(permutations(elements))

if __name__ == "__main__":
  elements = [1, 2, 3]
  print(all_permutations(elements))
  
# The script outputs:
# [(1, 2, 3), (1, 3, 2), (2, 1, 3), (2, 3, 1), (3, 1, 2), (3, 2, 1)]
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

24. What is the length of the output list if the input list has 5 numbers?

| Provide your answer here. |
| ------------------------- |
| ?                         |

25. What is the computational complexity of the following script?

The script uses the `bubble_sort` and the `binary_search` functions.

```
if __name__ == "__main__":
  data = [10,2,4,6,22,3,55,12]
  print(binary_search(bubble_sort(data), 10))
```

| Provide your answer here. |
| ------------------------- |
| ?                         |

### BDA Seminar 1 - Part 2

**Complete the following exercises on creating small programs.**

1. Examine the following code. The script calculates the time needed to run the `all_permutations` function.

```python
import time
from itertools import permutations

def all_permutations(elements):
    return list(permutations(elements))

if __name__ == "__main__":
  elements=[1,2,3,4,5,6,7,8,9,10,11]  
  # Start the timer
  start = time.time()
  result = all_permutations(elements)
  # End the timer
  end = time.time()
  
  print(f'Total time to run (seconds):',round(end-start,4))
```

2. Let's begin by downloading our initial large file, the Common Password List (`rockyou.txt`). Download the file from [Common Passwords List in Kaggle](https://www.kaggle.com/datasets/wjburns/common-password-list-rockyoutxt). 
   * Download the file and save it in the same directory as your Python script.
3. Examine the following script. The script extracts each line of our file using the `strip` that removes any leading or trailing whitespace.

```python
if __name__ == "__main__":
  with open('rockyou.txt', 'r',encoding='ISO-8859-1') as file:
    for line in file:
      # Strip newline and whitespace from the line
      current_password = line.strip()
      print(current_password)
      break
```

> [!TIP]
>
> ISO 8859-1 is the ISO standard Latin-1 character set and encoding format.

4. How many passwords are in the file?

```python
# Provide your Python script here


```

> There are 14344391 passwords; make sure your result is correct.

> [!TIP]
>
> When working with files, use the `except FileNotFoundError` .

5. What is the computational complexity of the above script?

| Provide your answer here. |
| ------------------------- |
| ?                         |

6. Create a `search_password` function to search for a password in a given file.

```python
# Provide your solution here


```

7. Calculate the time to find:

* 1234
* 1233242432
* mary

8. Does your input affect the time complexity?

| Provide your answer here. |
| ------------------------- |
| ?                         |

**:mount_fuji: The following tasks are challenging.**

9. Create a script to find out if there are any duplicated records in the rockyou.txt file.

* Store your results in a list.
* For this script, you have to use a nested loop.

:clock1: Try only using the first 25 records. Otherwise, this script might run for hours!

Then, run it for the whole dataset. Is it ever finished?

```python
# Provide your solution here

def check_duplicates1(file_path):
    result=[]
    try:
        count=0
        # Open the file and read all lines into a list
        with open(file_path, 'r', encoding='ISO-8859-1') as file:
            records = file.readlines()

        # Clean whitespace and newlines from each line
        records = [record.strip() for record in records]

        # Compare each record with every other record
        num_records = len(records)
        for i in range(num_records):
            if count==25:
              break
            for j in range(i + 1, num_records):
                if records[i] == records[j]:
                    # print(f"Duplicate record found: {records[i],i}")
                    result.append(records[i])
            count+=1
        print(f"I stop to search in count: {count}")
        return result

        # If no duplicates are found after all comparisons
        print("No duplicate records found.")
        return False

    except FileNotFoundError:
        print("Error: The file does not exist.")
        return False
    except Exception as e:
        print(f"An error occurred: {e}")
        return False

if __name__ == "__main__":
    file_path = "rockyou.txt"
    check_duplicates1(file_path)

```

10. What is the space complexity?

| Provide your answer here. |
| ------------------------- |
| O(n)                      |

11. Create a script to find the duplicated records in the `rockyou.tx`t file.

- Use a set instead of a list to store your data.
- Print a set of the duplicated values at the end.

```python
# Provide your solution here

def check_duplicates2(file_path):
    seen = set()
    duplicates = set()

    try:
        with open(file_path, 'r', encoding='ISO-8859-1') as file:
            for line_number, line in enumerate(file, 1):
                record = line.strip()
                if record in seen:
                    duplicates.add(record)
                else:
                    seen.add(record)

        if duplicates:
            print("Duplicates found:")
            print(duplicates)
            return True
        else:
            print("No duplicates found.")
            return False

    except FileNotFoundError:
        print(f"The file {file_path} does not exist.")

if __name__ == "__main__":
    file_path = "rockyou.txt"
    check_duplicates2(file_path)
```

12. What is the time and space complexity of this script if you don't use a set? What is when using sets?

| Provide your answer here.                                    |
| ------------------------------------------------------------ |
| O(n^2) without                                               |
| O(n) with sets 😀 - but you used extra space - the seen set - still is O(n) space. |
