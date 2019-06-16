# A: Fastq maniplation  
## 1. Download "linux_prac_day3.fastq.gz" from github.  
## 2. Google the format of fastq file. Fastq is the basic output format of NGS data.  
## 3. How many sequences are in this file?
## 4. How long is each read in this file? Tou can believe the number of "length=" on the header but check all the sequences.  

# B: GTF file  
## 1. Download "danio_GRCz10_head.gtf". 
## 2. GTF is a major format to store the information about gene position. Google the format and sort with the position of each gene. Maybe you need to investigate another option of `sort`...  
## 3. How many gene ids are there in this file? See 9th field.  
## 4. How many gene names are there in this file?  
## 5. The number of gene ids and gene names will not be consistent. Which gene is the clue? This command might be useul in some cases...  
### *paste*: merge 2 files with field.  
`paste` merge 2 files by fields. `cat` can also be used to merge files but it's for merging by row.  
``` bash
    echo -e "a\na\na" > test.a
    echo -e "b\nb\nb" > test.b
    paste test.a test.b
```
