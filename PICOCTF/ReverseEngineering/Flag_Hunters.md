# Flag Hunters : This challenge deals with input sanitization. 

This challenge requires the use of **Netcat** to print a lyrical program which hides a refrain that isn't printed. 

https://play.picoctf.org/practice/challenge/472?category=3&page=1

## Step 1: Analyzing the Lyrical Program 

For example, when we run through this lyrical program, we see the same output being printed out. 

From the hints given on this program, we can see that part of the code is prone to subversion and unsanitized user input. 

<img width="482" height="570" alt="image" src="https://github.com/user-attachments/assets/824f1b2c-202e-4c77-8e69-de6798344169" />

**Hmm interesting, this code is shown to accept and repeat user input of 6 letters long...**
