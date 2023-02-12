# Lab Report 3

## Creation of grep-results.txt
```
find written_2 > results.txt
grep ".txt" results.txt > grep-results.txt
```

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
