This challenge requires usage of gdb. 
![image](https://github.com/user-attachments/assets/2ab6b150-2eef-49b0-8c93-a9c054204cd1)
![image](https://github.com/user-attachments/assets/74411b8b-2b58-40b6-9efe-0d03845d4f45)
In this case, we need to find the value of the EAX register at the end of the main function. 
You could essentially just set a breakpoint but where would you put the breakpoint. 
![image](https://github.com/user-attachments/assets/ae971357-5a8a-40da-8213-8e9e3c668243)
Looking at the functions on the screen, we can get started on the breakpoint for the main function in this case. 
After running disassemble main, we can see the output of the function. 
![image](https://github.com/user-attachments/assets/45e675ba-ad5e-4d50-a075-0c82fa533a12)
Now, we have found the value we need. 
