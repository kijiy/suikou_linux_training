# Easy practice!
### 1. Open your ubuntu. Check your current directory.  
### 2. Check the contents of your home directory. If you follow the text of the last session, you might have "work" directory. If not, make "work" directory.  
### 3. Make new directory named "practice_day2" and move into it.  

# Command trainin
## *-*: command option  
Each command has some options which enable detailed functions. For example,  
``` bash
    ls          #you dont find any output.
    ls -a       #you will find additional output. This "a" option shows hidden directories and files.
    ls -l -a    #Option "l" can show detailed information of existing files.
```

## *wget*: download file  
`wget` can be used to download file.  
**CAUTION: If you wanna download a lot of files from open database such as NCBI, DDBJ or SRA, you have to be a bit careful. If you access outside servers without intervals, your access might be regarded as CYBER ATTACK. In this case please ask Yoshitake-sensei or me before you start downloading.**  
``` bash
    wget [PASTE THE INTERNET URL OF FILE] #File is uploaded on github
```

## *gunzip*: Decompress gunzip file  
`gunzip` is used to decompress gunzip file. Gunzip is widely used decompress method which is denoted as "gz" at the file extention. Sometimes open dataset is decompressed using other method like bzip2 or zip. In this case, google the way to decompress.  
``` bash
    gunzip data1_day2.tsv.gz #This file is what you downloaded above.
```

## *head*: print first *n* lines of command output or files.  
`head` prints first *n* lines of command output or files. This command is used to do a brief check of file content. Very useful!  
``` bash
    head data1_day2.tsv
    head -n 20 data1_day2.tsv #default output lines are 10 and you can specify the output lines by the option of "n".
```

## *|(pipe)*: connect the previout output to tne next command
`|(pipe)` connect the previous outputs to the next command arguement. This concept is difficult to explain and trying by yourself would be the best.  
``` bash
    cat data1_day2.tsv | head       #In this case, this command is same with "head data1_day2".
```

## *grep*: extract lines which include specific patterns.  
``` bash
    grep "rs4947963" data1_day2.tsv
    grep -v "rs4947963" data1_day2.tsv          #"v" option extracts lines which do not include specified patterns.
    grep -v "rs4947963" data1_day2.tsv | head   #The output is so long that connecting to "head" or "less" using pipe might be better.
```  
You can also set text file for query.  
``` bash
    echo "rs4947963" > q1.txt
    echo "rs13227878" > q2.txt
    cat q1.txt q2.txt > q.txt   #File merge
    grep -f q.txt data1_day2.tsv
```

## *wc*: count words  
`wc` is used to count words. Especially, "wc -l" is useful to count total number of lines.  
``` bash
    wc -l q.txt
    grep -f q.txt data1_day2.tsv | wc -l
```

## *cut*: select specific columns  
``` bash
    grep "rs13227878" data1_day2.tsv | cut -f 1
```  
Default column separator is "tab" and if you wanna change it, use option "d".  
``` bash
    grep "rs13227878" data1_day2.tsv | cut -f 4 
    grep "rs13227878" data1_day2.tsv | cut -f 4 | cut -d "." -f 1
```

## *sort*: sorting rows in order.  
Sometimes sorting the file contents is important. In this case, `sort` is useful.  
``` bash
    head data1_day2.tsv | sort -k 6     #"k" option specify key column to sort.
```  
Default sorting is based on dictionary/increasing order. If you want to sort number or sort with increasing manner, "n(number)" or "r(reverse)" option is needed.  
Download data2_day2.txt from the github.  
``` bash
    cat data2_day2.txt      #check the file content
    sort data2_day2.txt     #maybe not sorted in expected order
    sort -n data2_day2.txt  #it works
    sort -nr data2_day2.txt #decreasing manner
    head data1_day2.txt | sort -k7nr    #better to remember the phrase "-k[column number]nr" to sort with specific numeric column in decreasing manner
```

## *uniq*: remove dupricated lines
`uniq` command remove dupricated lines.  
**Notice: You need to sort before uniq**  
``` bash
    cut -f 1 data1_day2.txt | sort | uniq
```


