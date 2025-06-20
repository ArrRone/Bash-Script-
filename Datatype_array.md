# Data Type and Array in Bash

## Data Type

- Unlike many other programming languages, Bash is dynamically typed, which means that variables do not have a fixed data type

Bash supports the following data types:

1. Strings - sequences of characters enclosed in quotes (either single quotes or double quotes)
2. Integers - whole numbers without a decimal point
3. Floats - numbers with a decimal point
4. Arrays - collections of values accessed using an index
5. Associative arrays - collections of key-value pairs, where the key is a string and the value can be of any type.


**Since Bash is dynamically typed, you do not need to specify the data type of a variable when you declare it.**

- Example

```bash
name="John Smith"  # string type
age=30             # integer type
price=9.99         # float type
```

## Arrays

There are two type of arrays in bash:

- Indexed Arryas
- Associated Arrays


## Indexed Arrays 

- An indexed array is a collection of elements that are indexed by a numeric value, starting from zero. (In Z Shell- start from 1)

- In Bash, you can create an indexed array by simply assigning values to consecutive indices of a variable name enclosed in parentheses


**Example**

``` bash 
my_array=("apple" "banana" "orange")

echo ${my_array[0]}   # Output: apple
echo ${my_array[1]}   # Output: banana
echo ${my_array[2]}   # Output: orange
```

## Associative arrays

- An associative array is a collection of elements that are indexed by a string value instead of a numeric value.

- . In Bash, you can create an associative array by using the declare command with the `-A` option

**Example**

```bash
declare -A my_array
my_array["fruit1"]="apple"
my_array["fruit2"]="banana"
my_array["fruit3"]="orange"

# For value

echo ${my_array["fruit1"]}   # Output: apple
echo ${my_array["fruit2"]}   # Output: banana
echo ${my_array["fruit3"]}   # Output: orange

# For Key

echo "${!my_array[@]}"


```
