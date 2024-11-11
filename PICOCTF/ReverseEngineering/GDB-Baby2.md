# GDB Challenge: Finding the EAX Register Value

This challenge requires the use of **GDB** to inspect the value of the `EAX` register at the end of the `main` function.

![image](https://github.com/user-attachments/assets/0611a4b5-a33b-4dd2-9eb2-4804e76e8c08)


## Step 1: Setting a Breakpoint

![image](https://github.com/user-attachments/assets/0ddf1754-13c9-417f-89eb-d67017d3a367)

In this case, we need to find the value of the `EAX` register at the end of the `main` function. 

You could set a breakpoint in GDB, but the question is: **Where should you place the breakpoint?**

## Step 2: Analyzing the Functions

![image](https://github.com/user-attachments/assets/418c27ca-ebcd-41da-94bc-44439e044c17)

Looking at the functions on the screen, we can get started on setting the breakpoint for the `main` function. 

### Step 3: Disassembling the Main Function

To identify where we need the breakpoint, we use the following GDB command:

![image](https://github.com/user-attachments/assets/8a87a706-5815-4626-a13f-5a12e5b07f53)

The disassembled output will show us the instructions executed within the `main` function.

![image](https://github.com/user-attachments/assets/fd7a0deb-da11-4ed0-978c-f314437cee4f)


## Step 4: Finding the Value of EAX

After running the disassembly, we can analyze the code and find the point where we need to examine the `EAX` register. This is where we would set the breakpoint to stop the execution and inspect the value of `EAX`.

Now, we have successfully located the value we needed.
