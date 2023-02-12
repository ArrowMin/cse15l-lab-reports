# Lab Report 3

## Creation of results.txt
```
find written_2 > results.txt
```
*Contains directories and .txt files of written_2*
## Creation of grep-results.txt
```
find written_2 > results.txt
grep ".txt" results.txt > grep-results.txt
```
*Only contains .txt files of written_2*
## grep -c
### Example 1
```
$ grep -c "Bahamas" grep-results.txt 
4
```
### Example 2
```
$ grep -c ".txt" grep-results.txt 
224
```
### Explanation
Instead of giving the path names of each file with the input, adding the -c flag to grep will simply give the number of files that have that string. Useful if you just need the number of files.

## grep -v
### Example 1
```
$ grep -v ".txt" results.txt 
written_2/
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Castro
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Rybczynski
written_2/travel_guides
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz2
```
### Example 2
```
$ grep -v ".txt" grep-results.txt
 
```
### Explanation
The -v flag will match everything that is NOT containing the given string, for example when looking into the results.txt file for ".txt", only the directories are returned as they are the only things without ".txt" in them. Similarly, when using grep -v ".txt" on the grep-results.txt which only contains ".txt" files, nothing is returned as they all have it. Useful if you want to search for things that do not contain a certain string.
## grep -i
### Example 1
```
$ grep -i "bahamas" grep-results.txt 
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```
### Example 2
```
$ grep -i "BAHAMAS" grep-results.txt 
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```
### Explanation
Using the -i flag will make grep ignore case distinction, for example both "BAHAMAS" and "bahamas" resulted in finding files that contained "Bahamas". Useful if the files you are searching are named correctly but not capitalized consistently. 
## grep -m *number*
### Example 1
```
$ grep -m 3 "Bahamas" grep-results.txt 
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
```
### Example 2
```
$ grep -m 5 ".txt" grep-results.txt 
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
```
### Explanation
Using the -m flag with a number value argument will stop searching for the files that match the string once the number of files found matches the number given. This is useful if you just need the first few results of a search and do not want your terminal filled with a potential gigantic wall of text.

## Source for all commands
[https://linuxcommand.org/lc3_man_pages/grep1.html](https://linuxcommand.org/lc3_man_pages/grep1.html)

I found this source by looking up the man or manual documentation for the command "grep"
