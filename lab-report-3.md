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
Instead of giving the path names of each file with the input, adding the -c flag to grep will simply give the number of files that have that string.

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
The -v flag will match everything that is NOT containing the given string, for example when looking into the results.txt file for ".txt", only the directories are returned as they are the only things without ".txt" in them. Similarly, when using grep -v ".txt" on the grep-results.txt which only contains ".txt" files, nothing is returned as they all have it.
