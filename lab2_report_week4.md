# Lab report 2
## bug & fix 1
The following is the change we made to fix the bug. 
![update1](https://user-images.githubusercontent.com/55153144/151636916-84163292-72b4-47ab-b3b7-e7964216aa76.png)
And the following link is the testfile we used to cause the bug, we put some line that do not include "\[" in the test file. 
[testfile-2](https://pei-lu.github.io/markdown-parse/test-file2.html)
![symptom](https://user-images.githubusercontent.com/55153144/151637089-a78dcaf9-7fcf-4291-956d-b4905af34aff.png)
Th summarise for the bug: for this bug, our while loop is triying to look for a \[ some where in the line, however, it wasn't able to do so. This caused our program ran into a a infinite loop, untile the memory space ran out. 

## bug & fix 2
the following is my attemption to fix another bug.
![update2](https://user-images.githubusercontent.com/55153144/151639507-8bd4aa1f-6c09-47d3-98bf-5338b26c9b13.png)
this [link](https://pei-lu.github.io/markdown-parse/test-file3.html) is what promoted me to make this edition. <br/> The following is how the frogram fail
![symptom2](https://user-images.githubusercontent.com/55153144/151638877-2dbbd2a3-a1ff-4058-95fe-2d034fb12e08.png)
Because there isn't a close Parentheses, the index of it is -1, but a index out of bound exception was thrown for the substring method. because there is no way to take a sub string have a index form positive nomber to negative. In order to solve this bug, I just checked all the necessary element for a link, if any part missing, the line just going to be ignored, so that the program won't try to take a sub string with a index of -1.

## bug & fix 3
this is my third attemption to fis some bugs.
![update3](https://user-images.githubusercontent.com/55153144/151639957-beadd347-4b0d-4a31-a6b4-dce558af810b.png)
The this [test-file4](https://pei-lu.github.io/markdown-parse/test-file4.html) prompted me to make this change.
The symptom of this bug is reletively similer to the previous onw. the case is, even a line could have all the elemet for a link, the order of each element might be massed up. <br/>
![symptom3](https://user-images.githubusercontent.com/55153144/151640071-381a5a89-9f9a-42dd-84b3-e84d09d4d5e1.png)

The reason for this bug is same as the previous one. however, it is caused by different input. When the program searching for "\]","\(" or "\)", it starts at the index following the previous sign, in this case, it is possible for a string to have all the element but have -1 as the return of the "indexOf()"method.To fix the problem, I made changes that as long as the indexOf method call for any of the elemeent of a link is -1(make it not link) the program would ignor this line and jump to the next line.


