
### Qn1. Remove duplicate words from the file (grep/sed/awk can be used)
#### Input file
sample input file:
```sh
$ cat inputs/sample-input 
double double toil and trouble
fire burn and cauldron bubble bubble
tomorrow and tomorrow and tomorrow
creeps in this this petty pace from day toto day
to the last syllable of recorded time time
```
#### Command:
```sh
$ cat q1.sh
#!/bin/bash
# $1 can be set instead of input file with complete path
sed -r 's/(\w+)\s*\1/\1/g' $1 >stdout  2>stderr
```
#### execution: 
```sh 
$ cat inputs/sample-input | ./q1.sh
```
#### Output:
```sh
$ cat stdout
double toil and trouble
fire burn and cauldron bubble
tomorow and tomorow and tomorow
creps in this pety pace from day to day
to the last sylable of recorded time
```
