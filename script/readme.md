# data_collector.py
August 21st, 2016
Axel Garcia (axel.garcia@edu.uag.mx)

## Introduction
This is a Python script which has been created to collect performance data for several phonetic algorithms:
* Russel Index
* Soundex
* Daitch-Mokotoff Soundex
* Kölner Phonetik
* NYSIIS
* MRA
* Methaphone
* Double Metaphone
* Caverphone
* Alphasis
* Fussy Soundex
* Phonex
* Phonem
* Phoenix
* SfinxBis
* Phonet
* SPFC
* Beider-Morse Pontic Markig

### Input-Output Specification

* Input: The script takes as input a dictionary of terms. 
* Output: 
··* Phonetic Codes: A series of directories which contain files with the phonetic codes for each one of the terms in the dictionary. Each file holds a single phonetic code and it is named as the phonetic code also; e.g. phonetic_algorithm(“MyWord”) = 0022, then there is going to be a directory called “phonetic_algorithm” and a file “phonetic_algorithm/0022” which contents are the text “0022” (ASCII).
··* Results files: Results of the execution are saved to text files with Comma-Separated Value format. The file name of those files is “results_<algortihm name>.csv”. Data in those files has the following structure:

| Column# |  Description |
|:—-------:|-—-------—-------|
|    1   |  Number of the row in the natural language input file.|
|    2   |  Item Name of item.|
|    3   |  Phonetic code for item.|
|    4   |  Identified alternatives for item. This is a list of words separated by the colon (';') character.|
|    5   |  Precision of the phonetic algorithm for item.|
|    6   |  If the correct word is in the alternatives set.|
|    7   |  Phonetic algorithm name used.|

## Dependencies
The following dependencies can be installed in command line using the ‘pip’ command:
```
# pip install <package>
```

* [csv](https://pypi.python.org/pypi/csv)
* [numpy](https://pypi.python.org/pypi/numpy)
* [abydos](https://pypi.python.org/pypi/abydos)
* [chardet](https://pypi.python.org/pypi/chardet)

## Execution
This is a command line script. To execute it, please open a command line prompt and type:
```
$ python data_collector.py
```

Please have in mind that the script is verbose and will show debug messages as it is running.
