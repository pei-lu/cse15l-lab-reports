# lab 5 report
# How to found the tests with different results 
the way I found the difference is by using ```diff```. This method compair two file and return the line with different content.The following image is how to use diff.
  
![diffuse](https://user-images.githubusercontent.com/55153144/158082580-c9db5672-6f3c-43d7-b844-6aafae80779d.png)
  
the way to interpret the diff return:  
![difference](https://user-images.githubusercontent.com/55153144/158130275-b87a3761-15d5-43be-ba2a-2e9f49633c3b.png)  
  
48c48 meand the line 48 of two file are different;
\< means my markdown implementation have this retrun value.
\> mean the professor's implementation have this return value.

# test1
## **the different test result**  
   
![totest1](https://user-images.githubusercontent.com/55153144/158126391-85df1796-52b4-43e3-9357-04677f59c493.png)  
the line 48 is different. which indicates 
![problemFile1](https://user-images.githubusercontent.com/55153144/158126660-bdd9660a-2a29-4520-ae6f-a78402bb5d3b.png)  
the 12.md have different returns. 
the content is:  
```
\!\"\#\$\%\&\'\(\)\*\+\,\-\.\/\:\;\<\=\>\?\@\[\\\]\^\_\`\{\|\}\~
should not be a link.
```
the professor's implement is correct, 12.md are basicly a bounch of nonesence signs( with escape character), they do not represent anything.  
  
## **fix idea**  
The issue of my implement is my code wasn't able to recognize escape character, instead it just retrun whatever in the"()".
![tofix1](https://user-images.githubusercontent.com/55153144/158129795-d3514c15-3994-4336-9c97-c590c2e90980.png)  
in the line to determing index of openParen and close oaren, it need to judge if there is an \ as escape character befor it.
  

# test2
## **the different test result**  
![totest2](https://user-images.githubusercontent.com/55153144/158131315-e055bcda-5495-4ea3-b0ee-35f8a881a877.png)  
this indicates line 650 two file have differents.  
![where2](https://user-images.githubusercontent.com/55153144/158131311-4aa93e3b-e6cc-4053-95d1-c52921c23d83.png)   
according to the above information the testfile 391.md is probelmatic.  
The content is:
```
**(**foo)
//should not be a link
```
the professor's implement is correct. 

## **fix idea** 
![problem](https://user-images.githubusercontent.com/55153144/158133273-fda96484-5883-4597-928f-665f0c2b7f1b.png)  
in this implementation, there isn't a restriction for where the ] should be. The best way to fix is adding a boollean that only return true when index of ] is one smaller than(.and add the substring within the parentheses only when the bollean is true.
this boolean can also be affacted by where signs such as ! or \\. so that substring is added only when it is a link.  


