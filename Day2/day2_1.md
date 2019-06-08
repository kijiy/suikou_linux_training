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


