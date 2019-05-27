## Training of Linux commands

### *ls*: list the contents in a directory  
`ls` command can be used to see the contents in a directory. The term of directory is equal to the folder.  
``` bash
    ls          #maybe you can't find any outputs
```  

You can put the directory as an argument.  
``` bash
    ls /        #"/" means "root directory" which contains all files in the computer.  
    #Probabry you can see some contents.
```

### *mkdir*: make a directory  
`mkdir` command can be used to make a directory.  
``` bash
    mkdir work  
    ls    #Then you can find a new directory named "work".
```

``` bash
    mkdir work/practice_Day1  
    ls work    #Then you can find a new directory in work directory,
```

### *cd*: change a working directory
`cd` command can be used to change the working directory.  
``` bash
    ls    #Probably you will find the "work" directory.  
    cd work    #move into the "work".  
    ls    #Then you can find the "practice_Day1".
``` 

### *pwd*: **P**rint **W**orking **D**irectory  
`pwd` command can be used to check the absolute path of current directory.  
``` bash
    pwd    #You can know the path of the current directory.
    cd ~/work    #"~" is a special character which means the home directory.
    pwd    
```  
#### What is the absolute/relative path?  
The locations of files are described as path.
