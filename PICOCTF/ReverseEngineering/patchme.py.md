# Patchme.Py : Flag In the Same Directory

This challenge involves running a python program in the same directory as the encrypted flag given. 

<img width="528" height="389" alt="image" src="https://github.com/user-attachments/assets/b9c60e7b-b358-4bae-b3e1-020e95a208e3" />

## Step 1: Examining the Python File

In this case, we have two functions contained in this python file: str_xor and level_1_pw_check. 
**However, str_xor seems to be redundant in this case**
**level_1_pw_check could be something to look into..**

## Step 2: Analyzing the Functions

<img width="528" height="212" alt="image" src="https://github.com/user-attachments/assets/d452472e-4e9e-43fc-93bd-402da52a5347" />

Looking at the level_1_pw_check function, we are given a vague password breakdown for the function in this case.

**Hmmm, could the password for needed to decrypt the file be given to us...**
Let's try..

<img width="431" height="101" alt="image" src="https://github.com/user-attachments/assets/2766e12d-2c7e-4871-9844-48f8c0fe2e8e" />

**The flag works and we have a valid flag for this challenge**


Now, we have successfully located the value we needed.

