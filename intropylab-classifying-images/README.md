Date: 20190427
#python #module 

# Time

{{TOC}}

--- 

## Applications 

### Timing Performance of Code 

Timing your program or a portion of your program's code, allows one to compare the time costs associated with using different algorithms to solve a problem. Additionally, timing your code allows one to know the time costs associated with running a program using given computing resources.

To time your code In python requires the import of the `time()` function from the python *time* module. To simulate our program running for a certain period of time, we are going to use the time module's `sleep()` function. It will pause the program execution for a set number of seconds.

Since we only need to use the `time()` and `sleep()` functions, we will only import these two functions and not the entire time module. Only importing the functions from the module that you need saves on memory (RAM) your program requires to execute.

```python 
# Imports time() and sleep() functions from time module
from time import time, sleep
```

### Using Time and Sleep Functions

To time your code you will need to:

1. Create a variable that records the start time (`start_time`), the point you want to start timing your code
2. Create a variable that records the stop time (`end_time`), the point you want to stop timing your code
3. Finally, to calculate the total runtime (`tot_time`) by subtracting the `start_time` from `end_time`. Note `tot_time` will be the total time your code ran in seconds. 

```python 
# Sets start time
start_time = time()

# Replace sleep(75) below with code you want to time
sleep(75)

# Sets end time
end_time = time()

# Computes overall runtime in seconds
tot_time = end_time - start_time

# Prints overall runtime in seconds
print("\nTotal Elapsed Runtime:", tot_time, "in seconds.")
```


### Formatting Time

Likely you will want to format your runtime into a nice format like `hh:mm:ss` where:

- `hh` is two digit hours indicator
- `mm` is two digit minutes indicator
- `ss` is two digit seconds indicator

Recall the following regarding formatting time in seconds within python:

- 3600 seconds in an hour
- 60 seconds in a minute
- / (division operator) with int() function will return only the whole number part of a division
- % (modulo operator) returns the remainder of a division
- str() function converts numeric values into strings
- Lesson Data Types and Operators: Arithmetic Operators and Integers and Floats will help with formatting time in python.  

Using the information above provides the following format of total runtime, as `tot_time`:

- `hours = int( (tot_time / 3600) )`
- `minutes = int( ( (tot_time % 3600) / 60 ) )`
- `seconds = int( ( (tot_time % 3600) % 60 ) )`

```python 
# Prints overall runtime in format hh:mm:ss
print("\nTotal Elapsed Runtime:", str( int( (tot_time / 3600) ) ) + ":" +
          str( int(  ( (tot_time % 3600) / 60 )  ) ) + ":" + 
          str( int(  ( (tot_time % 3600) % 60 ) ) ) ) 
```



## Sources

[^1]: Source 1
[^2]: Source 2
[^3]: Source 3
[^4]: Source 4
Time Module 