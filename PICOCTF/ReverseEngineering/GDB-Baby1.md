GDB Challenge: Finding the EAX Register Value
This challenge requires the use of GDB to inspect the value of the EAX register at the end of the main function.
![image](https://github.com/user-attachments/assets/2ab6b150-2eef-49b0-8c93-a9c054204cd1)

Step 1: Setting a Breakpoint
![image](https://github.com/user-attachments/assets/74411b8b-2b58-40b6-9efe-0d03845d4f45)

In this case, we need to find the value of the EAX register at the end of the main function.

You could set a breakpoint in GDB, but the question is: Where should you place the breakpoint?

Step 2: Analyzing the Functions

![image](https://github.com/user-attachments/assets/ae971357-5a8a-40da-8213-8e9e3c668243)
Looking at the functions on the screen, we can get started on setting the breakpoint for the main function.

Step 3: Disassembling the Main Function
To identify where we need the breakpoint, we use the following GDB command:

css
Copy code
disassemble main
The disassembled output will show us the instructions executed within the main function.

![image](https://github.com/user-attachments/assets/45e675ba-ad5e-4d50-a075-0c82fa533a12)

Step 4: Finding the Value of EAX
After running the disassembly, we can analyze the code and find the point where we need to examine the EAX register. This is where we would set the breakpoint to stop the execution and inspect the value of EAX.

Now, we have successfully located the value we needed.

