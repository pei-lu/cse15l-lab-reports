# Lab 1 Labreport

## Installing Vscode 
I had previous experience with Vscode, indeed. All you have to do is to download it from internet and click install to install it.<br />
we can use this link to download [VScode](https://code.visualstudio.com/)

![image1-vscode](https://user-images.githubusercontent.com/55153144/149600439-1f6aa763-3a2e-4628-9509-3a7d59b60ec4.png)

## Remotely Connecting 
This part caused some trouble, because the password reset is a pain, sometimes the password would not reset, and I have to use my old password to log in instead of the new one. 
The procedure is represented below.
```
 $ssh + your account 
 enter the password// it would not been shown when you type it
 ```
 Then I am connected to the server.
![image2-connection](https://user-images.githubusercontent.com/55153144/149600459-1c76821c-4e20-4664-ac1f-9678f5461592.png)


## Trying Some Commands 
```
-ls
``` 
command was used to browse the files on the server, <br />
if attach -lat
```
ls -lat
```
all the hidden file would be shown and attach a directory could brows that file. Cd was used to change directory, cp was used to copy and cat was used to concatenate
<br />
![image3-ls](https://user-images.githubusercontent.com/55153144/149600463-574be108-17f1-4052-b02c-23273b3969df.png)


## Moving Files with scp 
```
scp WhereAmI.java cs15lwi22aji@ieng6.ucsd.edu:~/ 
```
was used to upload the java program to the server, in on my computer, it shows whare the file is stored, however when the program was run on the server, it shows it’s directory on there.
![image4-upload with scp](https://user-images.githubusercontent.com/55153144/149600469-a364870b-1427-40a7-bd70-59da50ac3ff8.png)


## Setting an SSH Key 
For setting up keys, we use 
```
ssh-keygen
```
we store the private key on our PC while store the public key on the server using SCP command. By the time I did the screen shot, I have already complete the process and not wanting to redo everything, but the key generating process should look like this.
![image5](https://user-images.githubusercontent.com/55153144/149600478-6f4ca08c-c383-4863-927a-707ce2375405.png)
this should be done in command prompt, the above is just an example.
![image5 1 myend](https://user-images.githubusercontent.com/55153144/149600581-41fa508e-8e2e-41b0-b466-bd0ad7597858.png)
this is where you shold do all the procedure. 



## Optimizing Remote Running 
Using up/down arrow or typing in multiple command at same line would make them run at same time, so and get the result all together.
![image6 ](https://user-images.githubusercontent.com/55153144/149600614-8c3aea46-e67c-44fd-99bb-808c2af8d9f4.png)

