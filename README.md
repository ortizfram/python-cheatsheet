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
    

