---
layout: page
title: baby crypto 
---

Here, we'll be diving into the basics and fundamentals of cryptography. Do note, this is partially CTF specific and is meant for learning purposes only. The programming language used will be Python3.
Now let's get started. 

**Challenge #1**:

You're given this string: 99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125

What do you do with it? The above is a string of ASCII characters. 

A decoding program can be: 

``` 
list = [99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]

for i in list:
    print(chr(i))
```
The first line of code is a list of all the numbers. We're simply iterating for each number within the list and converting them from an ASCII ordinal number to a character.

After running the script, we will get the following output which is the secret message/flag: _crypto{ASCII_pr1nt4bl3}_

**Challenge #2**:

You're given this string: 63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d

This time, it's a hex string.

A decoding program can be:

```
hex_string = "63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d"

print(bytes.fromhex(hex_string))
```
The first line is the hex string and we're essentially converting hex to bytes with the bytes.fromhex function.
After running the script, we get: _crypto{You_will_be_working_with_hex_strings_a_lot}_
