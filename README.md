# python-cheatsheet
# *️⃣textual data:
**message**

    message = 'Hello World'
## 🟡len

    print(len(message)) ⤵️
   11
## 🟡indexing
    print(message[10]) 
   d
## 🟡slicing
❗from 0 to 5 not including, spaces count too

    print(message[:5])
   Hello
## 🟡lower(),upper()
❗lower case, UPPERCASE

    print(message.lower())
    print(message.upper())
   hello world
   
   HELLO WORLD
## 🟡count()
❗must pass an argument

    print(message.count("l"))
    print(message.count("hello"))
   3
   
   1
## 🟡find()
❗ cause world starts at the 6th index, if `doesnt exist` `-1`

    print(message.find("World"))
    priont(message.find("universe"))
   6
   
   -1
## 🟡replace()
❗ returns a new string replaced, must assign a variable

**message** : "Hello World"

    a = print(message.replace("World","Universe"))
    print(a)
  Hello Universe
  
-------------------------------------------------
 ## 🟡 concatenate w format() & placeholders
    greeting = hi
    name =  Fanco
    message = greeting + " " + name
  hi franco
 
 ❗ `placeholders` are used to put variables inside strings
 
     greeting = hi
     name =  Fanco
     message = '{}, {}. Welcome!'.format(greeting, name)
 Hello, franco. Welcome!
 
 **or**
 
 ❗`f` in the beggining of string to say it's `format` , & vars directly inside placeholders `{variable}`
    
      message = f'{greeting}, {name.uppper()}. Welcome!'
   Hello, FRANCO. Welcome!
   
# *️⃣Numeric Data:
## 🟡type()
**arithmetic operators**

- addition : `+`

- subtraction: `-`

- multiplication: `*`

- Division: `/`

- Floor Division: `//` (no float results) 3//2 = 1

- Exponent: `**` 3**2 = 9

- Modulus: `%`   (gives reminder of division) 3 % 2= 1

❗ even : no reminder 2 % 2 = 0  // odd : reminder, 3 % 2 = 1

## 🟡abs()
❗ gives absolute value 

    print(abs(-3))
   3
## 🟡round()
    print(round(3.75))
   4

❗ you can specify how many round digits you want after the comma

    print(round(3.75, 1))
   3.8
   
## 🟡 comparisons: 
❗these are booleans

`==`	Equal	

`!=`	Not equal	

`>`	Greater than

`<`	Less than	

`>=`	Greater than or equal to	

`<=`	Less than or equal to

## 🟡 from string to number:
`int()` or `float()`

    num1= '100'
    num2= '200'
    print(num1 + num2)
   ❎ 100200
   
    num1= int()
    num2= int()
    print(num1 + num2)
   300
   
# *️⃣ Lists, Tuples, and Sets:
## 🟡list
    list = ['History', 'Math', 'Physics', 'CompScience']
### 🟠len()
❗gives how many elements are minside

    list = ['History', 'Math', 'Physics', 'CompScience']
    print(len(list))
   4
### 🟠indexing:
❗always from 0 

    print(list[0])
   History
   
    print(list[-1])
   CompScience
### 🟠 slicing:
    list = ['History', 'Math', 'Physics', 'CompScience']

❗ not including second, from 0 

❗ from 2 till end

    print(list[:2])
    print(list[2:])
   ['History', 'Math']
   
   ['Physics', 'CompScience']
### 🟠append()
❗ used to append 1 more at the end

    list.append('Art')
   ['History', 'Math', 'Physics', 'CompScience', 'Art']
### 🟠insert()
❗used to insert element in specific location `insert(0, 'Art')`

💁 to insert at the beginning 

    list.insert(0, 'Art')
   ['Art','History', 'Math', 'Physics', 'CompScience']
### 🟠 extend() 
❗ `extend`to add multiple values to a list

❗ cause if u use insert, it'll wiill create a double list [[]]

💁 extending list with list 2

    list = ['History', 'Math', 'Physics', 'CompScience']
    list2 = ['Art', 'Education']
    list.extend(list2)
    print(list)
   ['History', 'Math', 'Physics', 'CompScience', 'Art', 'Education']
### 🟠 remove(),pop()
❗`pop()` to remove last value of list , u also can asign a var to it and recall it

     list = ['History', 'Math', 'Physics', 'CompScience']

     list.remove('Math')
   ['History', 'Physics', 'CompScience']
    
     popped = list.pop()
     print(popped)
   ['History', 'Physics']
   
   CompScience
### 🟠sort(),reverse(),min(),max():
💁`reverse()` list

    list.reverse()
    print(list)
   ['CompScience', 'Physics', 'Math', 'History']
   
💁`sort()` list alphabetic, or numeric

    list = ['History', 'Math', 'Physics', 'CompScience']
    list.sort()
    print(list)
   ['CompScience', 'History', 'Math', 'Physics']
   
    nums = [1,5,3,6,4]
    nums.sort()
    print(nums)
   [1, 3, 4, 5, 6]
   
💁`sort(reverse=True)` sort backwards

    nums = [1,5,3,6,4]
    nums.sort(reversed=True)
    print(nums)
   [6, 5, 4, 3, 1]
   
💁`max()``min()`

    nums = [1,5,3,6,4]
    print(max(nums))
    print(min(nums))
   6
   
   1


    
   
