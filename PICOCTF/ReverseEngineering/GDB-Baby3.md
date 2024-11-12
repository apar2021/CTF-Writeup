# GDB Challenge: Finding the EAX Register Value

This challenge requires the use of **GDB** to inspect the value of the `EAX` register at the end of the `main` function.

![image](https://github.com/user-attachments/assets/0df26987-7268-4d62-85e0-d1e41e64e1aa)

## Step 1: Setting a Breakpoint

In this case, we need to find the value of the `EAX` register at the end of the `main` function. 

You could set a breakpoint in GDB, but the question is: **Where should you place the breakpoint?**

## Step 2: Analyzing the Functions

![image](https://github.com/user-attachments/assets/3a256742-d4cc-42b3-97a1-5eba4810acad)
![image](https://github.com/user-attachments/assets/705c4594-a8cf-494c-86c7-2020bb6ce880)

Looking at the functions on the screen, we can get started on setting the breakpoint for the `main` function. 

### Step 3: Disassembling the Main Function

To identify where we need the breakpoint, we use the following GDB command:
The disassembled output will show us the instructions executed within the `main` function.


## Step 4: Finding the Value of EAX

After running the disassembly, we can analyze the code and find the point where we need to examine the `EAX` register. This is where we would set the breakpoint to stop the execution and inspect the value of `EAX`.

Now, we have successfully located the value we needed.
