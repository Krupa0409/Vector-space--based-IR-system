# Vector-space--based-IR-system
The objective of this assignment is to build a vector space-based information retrieval system.
# Instructions for execution
## Dependencies

1. Hashedindex : can be installed via [pip](https://pypi.org/project/hashedindex/)
we have used Hashed index, efficient data structure for storing key value pairs.

```bash
pip install hashedindex
```
2. Spellchecker: can be installed via [pip](https://pypi.org/project/pyspellchecker/)

```bash
pip install pyspellchecker
```

## Steps-

1. index_creation.py
This file takes input of the 'wiki00' file of 'AO' folder shared with us.
for output this code will give 6 new files named as:
  - indt.json          --> Format { word  : {docid : tf}} 
	- indwot.json--> Format { word  : {docid : tf}} 
	- polt.json          --> Format { docid : {word  : tf}} 
	- polwot.json      --> Format { docid : {word  : tf}} 
	- title.json        --> Format { docid : titlename     
  - title_pl.json       -->Format{ docid : { titleterm : tf}
command line code
```bash
python index_creation.py filename
```
example
```bash
python index_creation.py wiki00
```
2. test_queries.py
This python 5 file uses the inverted index data structure already formed by the previous component of out code.
    indt.json, indwot.json, polt.json, polwolt.json, title.json 
It uses these data structures to calculate the score for each document for a particular user input query.
It provides the user with 4 different options to examine

	-Examine the working of the normal IR system ( with all modifications )
	-Examine the champion list modification
	-Examine the title term inclusion modification
	-Examine the query term overlap modification

It takes the user input as to what they want to examine
It will then take query from the user( prefer not to include any punctuation ) over which the code will run
It is programmed to show the user top 10 relevant documents if there are atleast 10 documents that have terms that match with query words.

command line code
```bash
python test_queries.py 
```
## Sample queries:
1. dutch-born environmentalist
2. s maruti rao
3. civil rights violated
4. American city to individually restrict cannabis
5. Ceo of brandyourself

## Other instrcutions:
	1)First make sure that all the 5 files mentioned above are present in the same folder as      of test_queries.py (I have already pasted the files required so 	that you can run the second part without even running the first part. However if you do run the first part make sure that you delete these files because 	then the filenames would clash)
	2)You will need a default python/python3 terminal
	3)Open the test_queries.py file using the python terminal.
	4)For some reason after taking both the inputs the code does not seem to work for the very first time( it autoejects)
	5)If point 4 happens then open the file again using the python terminal.
	6)This time it will work very fine
	7)The code has a while(True) statement which allows the user to examine different modifications of our IR system one after the other
	8)If at anytime you want to come out of the loop just press Ctrl + C and you will be ejected 
	9)You can also see the updatedss folder which contains screenshots of various multi term queries and their relevant documents
