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
179
```
