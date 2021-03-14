#NLP100
This repository consists code for tasks given NLP100
by Tokyo Institute of Technology.
https://nlp100.github.io/en/

#Chapter 2: UNIX Commands:
- 10 Line count: 
 
```bash 
   wc -l popular-names.txt   
``` 
- 11 Replace tabs into spaces:
```bash
   sed "s/\t/\s/" popular-names.txt > output.txt
```

- 12 col1.txt from the first column, col2.txt from the second column:
```bash
   awk -F \t '{ print $1 }' popular-names.txt > col1.txt && awk -F \t '{ print $2 }' popular-names.txt > col2.txt
```
- 13 Merging col1.txt and col2.txt:
```bash
   paste -d "\t" col1.txt col2.txt > merged_col1_col2.txt 
```
- 14 Last N lines:
```bash 
   head -2 popular-names.txt
```
- 15 Last N lines:
```bash
   tail -2 popular-names.txt
```
- 16 Split a file into N pieces.(Note: 15-split is prefix for file name):
```bash
   split -l 500 popular-names.txt 15-split
```
- 17  Distinct strings in the first column:
```bash
   cat popular-names.txt | awk '{ print $1 }' | sort | uniq
```

- 18 Sort lines in descending order of the third column:
```bash
   awk '{ print $3 }' popular-names.txt| sort -h
```
- 19 Frequency of a string in the first column in descending order:
```bash
   awk '{ print $1 }' popular-names.txt| sort | uniq -c | sort 
```
