# A: SNP data  
## 1. See "data1_day2.tsv". Print 1st line of this file. In this line, file discription is recorded. 
## 2. How many SNP records does this file contain?(Excluding header discriotion)  
## 3. Which record has the highest alternative base change frequency?  
## 4. "uniq -c" count the number of duplication. Print the friquency of all X to Y mutation pattern.
## 5. Which is the most likely T to C mutaion based on the HWE_p_value?

# B: aging data exploration  
## 1. Download "fileset_ex_day2.tar.gz" from github.  
## 2. Decompress the downloaded files. I didn't tell you how to decompress tar.gz, so google it. 
## 3. See "age.txt". This file is tab-delimited and each column shows scientific name, common name, max weight and maximum lifespan from left. Which is the heaviest species?  
## 4. Which is the longest-lived species?  
## 5. How many Genus in this list?  
## 6. What is the median value of maximum weight excluding unknown value?

# C: fasta handling  
## 1. See "danio.fa". This is the fasta-formatted zebrafish transcripts. In fasta format, each query block consists of ">" started header line and its DNA (or protein) sequence. How many queries does this danio.fa contain?  
## 2. Count and compare the numbers of transcripts and genes. Why the numbers are different? Trancript ID and gene ID are denoted as "ENSDART(ENSembl DAnio Ratio Transcript)" and "ENSDARG(ENSembl DAnio Rario Gene)".  
## 3. How many nucleotides does "ENSDART00000169803.2" have? This question is not so difficult but needs some kind of idea. Maybe this needs additional command I've not told you yet so google the command which satisfies your idea.  
