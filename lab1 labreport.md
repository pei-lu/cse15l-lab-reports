•	Installing Vscode
I had previous experience with Vscode, indeed. All you have to do is to download it from internet and click install to install it.

•	Remotely Connecting
This part caused some trouble, because the password reset is a pain, sometimes the password would not reset, and I have to use my old password to log in instead of the new one. Then type in the $ssh + your account then enter the password. Then I am connected to the server.  


•	Trying Some Commands
-ls command was used to browse the files on the server, if attach -lat, all the hidden file would be shown and attach a directory could brows that file. Cd was used to change directory, cp was used to copy and cat was used to concatenate

•	Moving Files with scp
scp WhereAmI.java cs15lwi22aji@ieng6.ucsd.edu:~/ was used to upload the java program to the server, in on my computer, it shows whare the file is stored, however when the program was run on the server, it shows it’s directory on there. 

•	Setting an SSH Key
For setting up keys, we use ssh-keygen, we store the private key on our PC while store the public key on the server using SCP command. By the time I did the screen shot, I have already complete the process and not wanting to redo everything, but the key generating process should look like this. 

•	Optimizing Remote Running
Using up/down arrow or typing in multiple command at same line would make them run at same time, so and get the result all together. 
