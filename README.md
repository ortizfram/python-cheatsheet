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
