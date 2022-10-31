Command:grep
 
first command option: 
```
-ls
```
First example
```
(base) jrd@Jiajies-MBP-3 911report % ls |grep chapter-1
```
```
chapter-1.txt.gz
chapter-10.txt
chapter-11.txt
chapter-12.txt
chapter-13.1.txt
chapter-13.2.txt
chapter-13.3.txt
chapter-13.4.txt
chapter-13.5.txt
```
Explaination:
The -ls option shows us the type of file that we look for, here we look for the file type that contains chapter-1 with it. We can see that chapter-1.txt are type of gz which is a compress file, and all the other files are text files.



Second example:
```
find -mtime +20

```
