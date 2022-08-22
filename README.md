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
## 🔴list
❗👁️‍**MUTABLE**

    list = ['History', 'Math', 'Physics', 'CompScience']
### 🟠len()
❗gives how many elements are minside

    list = ['History', 'Math', 'Physics', 'CompScience']
    print(len(list))
   4
### 🟠indexing, returning, IN(bool):
❗always from 0 

💁 `first value` in list `[0]`

    list = ['History', 'Math', 'Physics', 'CompScience']
    print(list[0])
   History
💁 `last value` in list `[-1]` 

    list = ['History', 'Math', 'Physics', 'CompScience']
    print(list[-1])
   CompScience
   
💁`returning index`

    list = ['History', 'Math', 'Physics', 'CompScience']
    print(list.index('Math'))
   1
  
💁 `in` boolean

    list = ['History', 'Math', 'Physics', 'CompScience']
    print('Art' in list)
   False
   
### 🟠 slicing:
    list = ['History', 'Math', 'Physics', 'CompScience']

❗ not including second, from 0 

❗ from 2 till end

    print(list[:2])
    print(list[2:])
   ['History', 'Math']
   
   ['Physics', 'CompScience']
 ### 🟠 join(), split()
 ❗`split()` will cut the spicified values you choose from the string and make it a list again
 
    list = ['History', 'Math', 'Physics', 'CompScience']
    
    list_str = ' - '.join(list)
    print(list_str)
    
    new_list = list_str.split(' - ')
   History - Math - Physics - CompScience
   
   ['History', 'Math', 'Physics', 'CompScience']
    
    
 
 ### 🟠 for loop   
💁`for loop + enumerate index` starting in 1

    list = ['History', 'Math', 'Physics', 'CompScience']
    
    #same as for item in list
    for index,item in enumerate (list, start = 1):
        print(index, item)
  1 History
   
  2 Math
   
  3 Physics
   
  4 CompScience
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
  
    nums = [1,5,3,6,4]
    nums.sort()
    print(nums)
   ['CompScience', 'History', 'Math', 'Physics']
   
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
## 🔴 tuple
❗ 👁️‍🗨️**IMMUTABLE** (can't append(), can't remove(), can't asign values)

    tuple = ('History', 'Math', 'Physics', 'CompSci
## 🔴 set
❗ 👁️‍🗨️**UNORDERED NO-DUPLICATES** (ORDER CHANGE IN EACH EXECUTION)
❗ set is optimize to check if value exist IN set

    set = {'History', 'Math', 'Physics', 'CompScience'}
### 🟠intersection(), difference(), union()
❗`intersection()` which `common` between `sets`

    cs_courses = {'History', 'Math', 'Physics', 'CompScience'}
    art_couses = {'History', 'Math', 'Art', 'Design'}
    
    print(cs_courses.intersection(art_courses))
   {'History', 'Math'}   
   
❗`difference()` which `difference` between `sets`

    
    cs_courses = {'History', 'Math', 'Physics', 'CompScience'}
    art_couses = {'History', 'Math', 'Art', 'Design'}
    
    print(cs_courses.difference(art_courses))
   {'Physics', 'CompScience'}
   
❗`union()` `all sets` from `both` united

     
    cs_courses = {'History', 'Math', 'Physics', 'CompScience'}
    art_couses = {'History', 'Math', 'Art', 'Design'}
    
    print(cs_courses.union(art_courses))
   #unordered
   {'History', 'Math', 'Physics', 'CompScience', 'Art', 'Design'}
## 🟡 creating empty set,tuple,list

    empty_list = list()
    empty_tuple = tuple()
    empty_set = set()
# *️⃣Dictionary
    student = {'name':'John','age':25,'courses':'Math''CompScience'}
    print(student['name'])
    print(student.get('age'))
   John 
   
   25
  ## 🟡 add new entry:
    student['phone'] = 555
    print(student['phone'])
   555
 ## 🟡update() values:
    student = {'name':'John','age':25,'courses':'Math''CompScience','phone' :555}
    student['name'] = 'jane'
   
    or 
    student.update({'name':'Jane','age': 27})
    
    print(student)
    print(student['age'],student['name'])
   {'name':'Jane','age':25,'courses':'Math','CompScience','phone' =555}
   
   Jane 27
   
## 🟡delete, pop()
    student = {'name':'Jane','age':25,'courses':['Math','CompScience'],'phone' =555}
    del student['phone']
    
    age = student.pop('age')
    
    print(age)
    print(student)
   student = {'name':'Jane','courses':'Math''CompScience'}
   
   25
 ## 🟡len()
    student = {'name':'Jane','courses':['Math','CompScience']}
    print(len(student))
   2
## 🟡print keys,values, or both
    student = {'name':'Jane','courses':['Math','CompScience']}
    
    print(student.keys())
    print(student.values())
    print(student.items())
   dict_keys(['name', 'courses'])
   
   dict_values(['Jane', ['Math', 'CompScience']])
   
   dict_items([('name', 'Jane'), ('courses', ['Math', 'CompScience'])])
   
 ## 🟡for loop
    for key, value in student.items():
        print(key, value)
   name Jane
   
   courses ['Math', 'CompScience']
     
# *️⃣Conditionals & booleans:
❗booleans start in `True`
## 🟡if,else,elif
    language = 'Python'
    if language == 'Python':
        print('Conditional was true')
    elif language == 'Java':
        print('language is java')
    elif language == 'JavaScript':
        print('language is js')
    else:
        print('no match')
   Conditional was true
 ## 🟡 and,or,not
     user = 'admin'
    logged_in = True

    if user == 'admin' and logged_in:
        print('admin page. Welcome')
    elif not logged_in:
        print('please log in ')
    else:
        print('bad creds')
# *️⃣Loop & iteration:
## 🟡break & continue:
    nums = [1,2,3,4,5,]
    for num in nums:
        if num == 3:
            print('was found')
            break
        print(num)
   1
   
   2
   
   was found
## 🟡range()
    for i in range(1,5):
        print(i)
   1
   
   2
   
   3
   
   4
   
 ## 🟡 while
       x = 0
       while x < 10:
           if x == 5:
               break
           print(x)
           x += 1
0

1

2

3

4
# *️⃣Funtions:
👁️‍🗨️ ❗ DON't REPEAT YOURSELF **KEEP IT DRY**
## 🟡def
    hello_funct():
        print('hello man')    #printing
    hello_funtion()
    
    
    hello_funct2():
        return 'Hello mannnn'    #returning
    print(hello_funt2().upper()) 
hello man

HELLO MANNNN
## 🟡scoped arguments FORMAT:
💁asking for `greeting` message & `name`. `If you not passing name`, there's a `default name value` `='you'`

    def hello_funct(greeting, name = 'you'):
        return  f'{greeting}, {name}'

    print(hello_funct('Hi','Franco'))
   Hi, Franco
## 🟡 unpack values:
    def student_info(*args,**kwargs):
        print(args)
        print(kwargs)

    courses = ['Math','Art']
    info = {'name': 'Franco', "age":21}

    student_info(*courses,**info)
('Math', 'Art')

{'name': 'Franco', 'age': 21}

# *️⃣Importing modules:
❗ you 're importing module from an other document, go to the to of the file & import module from same directory 
`module_name=``document name`
## 🟡importing
 **module**
    
    #my_module
    print('Imported my_module...')

    test = 'Test String'

    def find_index(to_search, target):
        '''Find the index of a value in a sequence'''
        for i, value in enumerate(to_search):
            if value == target:
                return i

        return -1
**apply module**
    
    import my_module as mm
    
    courses = ['History', 'Math', 'Physics', 'CompSci']
    
    index = mm.find_index(courses, 'Math')
    print(index)
    
   imported my_module...
   
   1
   ## 🟡 adding new directory to sys.path
   ❗ you do this if module isn't in same directory
   
   ### 💁 from the ide type
   
        sys.path.append('\C:\Users\User\Documents\workspace\my_modules')
    
   ### 💁 from system do this:
   
   - computer > properties

   - advanced  sys settings

   - Environment variables >> create new

   - name = `PYTHONPATH`,  location = `\C:\Users\User\Documents\workspace\my_modules`  #unique for own machine

   - CMD : import (module name)

   - type : `sys.path` to check f location was added as first line
    
## 🟡 random library
    import random 
    
    courses = ['History', 'Math', 'Physics', 'CompSci']
    
    random_course = random.choice(courses)
    print(random_course)
   Math
# *️⃣CSV module:
❗ comma separated values

`first_line = ` column names

    first_name,last_name,email
    John,Doe,john-doe@bogusemail.com
    Mary,Smith-Robinson,maryjacobs@bogusemail.com
    Dave,Smith,davesmith@bogusemail.com
    Jane,Stuart,janestuart@bogusemail.com
    Tom,Wright,tomwright@bogusemail.com
    Steve,Robinson,steverobinson@bogusemail.com
    Nicole,Jacobs,nicolejacobs@bogusemail.com
    Jane,Wright,janewright@bogusemail.com
    Jane,Doe,janedoe@bogusemail.com
    Kurt,Wright,kurtwright@bogusemail.com
    Kurt,Robinson,kurtrobinson@bogusemail.com
    Jane,Jenkins,janejenkins@bogusemail.com
    Neil,Robinson,neilrobinson@bogusemail.com
    Tom,Patterson,tompatterson@bogusemail.com
    Sam,Jenkins,samjenkins@bogusemail.com
    Steve,Stuart,stevestuart@bogusemail.com
    Maggie,Patterson,maggiepatterson@bogusemail.com
    Maggie,Stuart,maggiestuart@bogusemail.com
    Jane,Doe,janedoe@bogusemail.com
    Steve,Patterson,stevepatterson@bogusemail.com
    Dave,Smith,davesmith@bogusemail.com
    Sam,Wilks,samwilks@bogusemail.com
    Kurt,Jefferson,kurtjefferson@bogusemail.com
    Sam,Stuart,samstuart@bogusemail.com
    Jane,Stuart,janestuart@bogusemail.com
    Dave,Davis,davedavis@bogusemail.com
    Sam,Patterson,sampatterson@bogusemail.com
    Tom,Jefferson,tomjefferson@bogusemail.com
    Jane,Stuart,janestuart@bogusemail.com
    Maggie,Jefferson,maggiejefferson@bogusemail.com
    Mary,Wilks,marywilks@bogusemail.com
    Neil,Patterson,neilpatterson@bogusemail.com
    Corey,Davis,coreydavis@bogusemail.com
    Steve,Jacobs,stevejacobs@bogusemail.com
    Jane,Jenkins,janejenkins@bogusemail.com
    John,Jacobs,johnjacobs@bogusemail.com
    Neil,Smith,neilsmith@bogusemail.com
    Corey,Wilks,coreywilks@bogusemail.com
    Corey,Smith,coreysmith@bogusemail.com
    Mary,Patterson,marypatterson@bogusemail.com
    Jane,Stuart,janestuart@bogusemail.com
    Travis,Arnold,travisarnold@bogusemail.com
    John,Robinson,johnrobinson@bogusemail.com
    Travis,Arnold,travisarnold@bogusemail.com
## 🟡 import:
    import csv
## 🟡 read:
❗ same directory:

💁asiggning alias to csv.reader, `next()` `will ommit`  first line `column names`, & printing list with a for loop

    with open('names.csv','r') as csv_file:
        csv_reader = csv.reader(csv_file)
        
        next(csv_reader)
        
        for line in csv_reader:
            print(line[2]) #printing just emails[2]
## 🟡 write to a csv:
💁 for loop is for rewriing in a new file with slash separated values 

    import csv
    
    with open('names.csv','r') as csv_file:
        csv_reader = csv.reader(csv_file)
        
        with open('new_names.csv','w') as new_file:
            csv_writer = csv.writer(new_file, delimiter= '-')
            
             for line in csv_reader:
                 csv_writer.writerow(line)
  first_name-last_name-email
  
  Jhon-Doe-"jhondoe@gmail.com"
  
  mary-smith-"marysmith@hotmail.com"
                
