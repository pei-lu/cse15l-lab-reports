# Lab report 2
## bug & fix 1
The following is the change we made to fix the bug. 
![update1](https://user-images.githubusercontent.com/55153144/151636916-84163292-72b4-47ab-b3b7-e7964216aa76.png)
And the following link is the testfile we used to cause the bug, we put some line that do not include "\[" in the test file. 
[testfile-2](https://pei-lu.github.io/markdown-parse/test-file2.html)
![symptom](https://user-images.githubusercontent.com/55153144/151637089-a78dcaf9-7fcf-4291-956d-b4905af34aff.png)
Th summarise for the bug: for this bug, our while loop is triying to look for a \[ some where in the line, however, it wasn't able to do so. This caused our program ran into a a infinite loop, untile the memory space ran out. 

## bug & fix 2
the following is my attemtation to fix another bug.

![symptom2](https://user-images.githubusercontent.com/55153144/151638877-2dbbd2a3-a1ff-4058-95fe-2d034fb12e08.png)
