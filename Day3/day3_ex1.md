# A: aging data exploration  
## 1. Download "fileset_ex_day2.tar.gz" from github.  
## 2. Decompress the downloaded files. I didn't tell you how to decompress tar.gz, so google it. 
## 3. See "age.txt". This file is tab-delimited and each column shows scientific name, common name, max weight and maximum lifespan from left. Which is the heaviest species?  
## 4. Which is the longest-lived species?  
## 5. How many Genus in this list?  
## 6. What is the median value of maximum weight excluding unknown value?

# B: fasta handling  
## 1. See "danio.fa". This is the fasta-formatted zebrafish transcripts. In fasta format, each query block consists of ">" started header line and its DNA (or protein) sequence. How many queries does this danio.fa contain?  
## 2. Count and compare the numbers of transcripts and genes. Why the numbers are different? Trancript ID and gene ID are denoted as "ENSDART(ENSembl DAnio Ratio Transcript)" and "ENSDARG(ENSembl DAnio Rario Gene)".  
## 3. How many nucleotides does "ENSDART00000169803.2" have? *wc* command and this command would be useful.  
### *tr*: remove/replace characters  
`tr` command must be used after the pipe connection.  
``` bash
    [output] | tr -d "[character]"  #To remove a specific character  
    [output] | tr "[target]" "[replacement]"  #To replace characters  
    echo "abcd" | tr -d "d"  
    echo "abcd" | tr "c" "\n"  #Insert linefeed code
```

