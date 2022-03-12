# Lab report4
## Markdown Parse links
[link]() to my respounstory</br>
[link](https://github.com/Alexander-Kourjanski/markdown-parse) to the group we reviewed. 

<!-- ## supposed return
![snippet1-2](https://user-images.githubusercontent.com/55153144/155933701-7eefdce5-2fe7-441f-862d-3bb9cc7ad3db.png)
```
snippet1
[`google.com, google.com , ucsd.edu]

snippet2
[a.com, a.com(()), example.com]
```
![snippet3](https://user-images.githubusercontent.com/55153144/155933732-6f82c9c7-45dd-40f1-8a35-83940fead32d.png)
```
snippet3
[https://ucsd-cse15l-w22.github.io/]
```
the above represent the supposed out put of each snippet. -->

<!-- ## My markdown return
![ourgroup](https://user-images.githubusercontent.com/55153144/155936597-11cde9e3-2c95-4496-839e-687e3628d69d.png)
all three test failed 

## Revied in week 7
![reviewedgroup](https://user-images.githubusercontent.com/55153144/155937220-36946b81-7b4c-4383-8c96-a4c1a7d74d7a.png)
all 3 test failed too. -->
# Snippet 1
## 1. expect return from [commonmark](https://spec.commonmark.org/dingus/)
![7DB6@C 5OVTZ_ P9UW~5Y10](https://user-images.githubusercontent.com/55153144/157958957-6c6696f1-1e6e-48d3-b1e8-a507f99033ed.png)
the return shoule be
```
[`google.com, google.com , ucsd.edu]
```
## 2. the test run
![Test1](https://user-images.githubusercontent.com/55153144/157967303-543bec63-c016-414b-9904-cbc74ca27477.png)

## 3. Test result for my implement
</br>

![result1](https://user-images.githubusercontent.com/55153144/157967985-b6480925-4d60-4225-a836-4fba48e36090.png)
 
 the test fail because `[a link`](url.com) was not a link but is was recognized as one. because the appearence of both"[]" and "()"



## 4. Test and result form my reviewed 
test of Alex's markdown parse
![ZXEKNTDJ }3RQH)PQ64CE%J](https://user-images.githubusercontent.com/55153144/157984149-48b83f60-d062-4362-aa8a-a8fee0ea1e23.png)

test result

![2_JH O{UN%0~JN8CYZIJ_F8](https://user-images.githubusercontent.com/55153144/157984238-b6be4efe-628f-4684-9079-c84ab86e3d06.png)

the test also failed, because his implementatoion also recognize `[a link`](url.com) as a link, which is not 

# Snippet 2
## 1. expect return from [commonmark](https://spec.commonmark.org/dingus/)
 ![46U~(I${8H@)2I$9(D_XL`L](https://user-images.githubusercontent.com/55153144/157984491-b21581c2-6420-4fa5-8ae2-5e151bbd92c5.png)
```
snippet2
[a.com, a.com(()), example.com]
```
## 2. the test run

![0{1KI}HNTK(X){2L))FAV8](https://user-images.githubusercontent.com/55153144/157984836-4e5b5f5b-151f-4db8-8a9f-74b5df1ef6af.png)
the above is my implementation of the test

## 3. Test result for my implement
</br>

![GLG@_OK $F4FB{}RHKFG~XS](https://user-images.githubusercontent.com/55153144/157985300-fec3b429-97a2-4c96-b56b-83fb98fb716d.png)
the test faild, because my markdownParse stop record the link at the first appearence of), instead of the last one, as it supposed to

## 4. Test and result form my reviewed 
test of Alex's markdown parse
![BQ06W9C8LG2MU${ `TA4IZL](https://user-images.githubusercontent.com/55153144/157986025-16cfc095-785a-44e6-ab66-51fd046736b6.png)

test result
![QVJFQ6A)9(DY}B@_`U9RBC0](https://user-images.githubusercontent.com/55153144/157985756-4e92f68d-b1ec-4de1-bd07-55512f40f259.png)

his test failed as well, because the link sublis is also stoped at first (). His implementation alco can not parse the linkname with [] need to be skiped.


# Snippet 3
## 1. expect return from [commonmark](https://spec.commonmark.org/dingus/)
![D4A~9%P6MCO~97W{B7ER MV](https://user-images.githubusercontent.com/55153144/157986450-1ad75cfd-dd1f-4a73-9ac9-c858b5200651.png)

```
snippet3
https://ucsd-cse15l-w22.github.io/
```
## 2. the test run
![QL9W$R2L}@IV)9DWIXE(S~S](https://user-images.githubusercontent.com/55153144/157987338-efd81f60-220a-48fd-be34-e52fbd3a8666.png)

## 3. Test result for my implement
</br>

![2MI8 (CR 2QMB$KQ8$QPTPD](https://user-images.githubusercontent.com/55153144/157987447-651b6dd6-8de9-4a95-b847-610f71ae52a8.png)
Our implementation faild this test because we parse the document by lines. if the link exceed more than one line, then our program would be able to parse it.


## 4. Test and result form my reviewed 
test of Alex's markdown parse
![3620}6U1 W`RTZ5OC46{Q}3](https://user-images.githubusercontent.com/55153144/157987061-7b4d380c-cb08-4926-b983-7739efba2b7b.png)

test result
![E K$DJSR`JT`%U7%S3_28E5](https://user-images.githubusercontent.com/55153144/157986759-6619ce33-47d6-456f-bc3c-8678436b8a48.png)
His implement failed, because this implementation fail to recognize the line break within the titile and fail to stop where the link have no closing ).

# Q1 small change to improve for snippet 1

one of the easiest way to deal with the bug is to adding a rule which defined the index of "`[" and ignor as a "[". Because it was used to hilight a text and break the text up into different section. the "[]"are no longer consider a pair. So what I need to do is to confirm the brecket are both out side the dot.

## Q2 small change to improve for snippet 2
this would be a kind easy fix, we could import the stack data structure, and only find the last brecket or 
Parentheses as the end of link. By using this method, the entire link woule be included in the returned value.

## Q3 small change to improve for snippet 3
This would not be a quick fix. Because our entire markdown-parse was structured based on the content could be break down by lines, we are actually parsing each line instead of the whole document. If there is a link that exceed one line, our markdown-parse would not work. And the entire program need to be rewrite. 
