# Training of Linux commands

## *ls*: list the contents in a directory  
`ls` command can be used to see the contents in a directory. The term of directory is equal to the folder.  
``` bash
    ls          #maybe you can't find any outputs
```  

You can put the directory as an argument.  
``` bash
    ls /        #"/" means "root directory" which contains all files in the computer.  
                #Probabry you can see some contents.
```

## *mkdir*: make a directory  
`mkdir` command can be used to make a directory.  
``` bash
    mkdir work  
    ls          #Then you can find a new directory named "work".
```

``` bash
    mkdir work/practice_day1  
    ls work     #Then you can find a new directory in work directory,
```

## *cd*: change a working directory
`cd` command can be used to change the working directory.  
``` bash
    ls          #Probably you will find the "work" directory.  
    cd work     #move into the "work".  
    ls          #Then you can find the "practice_day1".
``` 

## *pwd*: **P**rint **W**orking **D**irectory  
`pwd` command can be used to check the absolute path of current directory.  
``` bash
    pwd         #You can know the path of the current directory.
    cd ~/work   #"~" is a special character which means the home directory.
    pwd    
```  
#### What is the absolute/relative path?  
The locations of files are described as path. Path can be written in 2 ways: absolute and relative path. Let's see the example.  
``` bash
    cd ~/work   #Move into the work directory.
    pwd         #Make sure you are in the work directory.
```  
Now you are in the work directory. When you excute `ls`, you will find the "practice_day1" directory. To enter the practice_day1 directory, you can put the path to `cd` argument in 2 different ways. In one way,  
``` bash
    cd practice_day1
```  
This is called relative path. Relative path is short and simple, but can be used only at your current directory. For example,  
``` bash
    cd ~        #Move into the home directory.
    cd practice_day1        #Then this command cannot be used because you changed the working directory.
    cd work/practice_day1   #This command should work but is still a relative path.
```  
The other way, you can chose the absolute path. Absolute path is the path which is available at any current directory. For example,  
``` bash
    pwd         #Make sure you are in practice_day1. If not, please excute the commands above. This "pwd" output is the absolute path.
    cd ~        #This "~" is the absolute path. You can sepcify the home directory by this character wherever you are.
    cd practice_day1        #This relative path is not available as I mentioned above.
    cd /absolute/path/you/got/above       #You can!
```  
The concept of absolute/relative path is shown below.  
<img src="https://github.com/kijiy/suikou_linux_training/blob/images/image/path_image.001.jpeg" width="600px">  
To better understand the structure of file system, "tree" command is useful. "tree" is not implemented in default, you need to install it by yourself. For ubuntu users,  
``` bash
    sudo apt install tree #sudo means you excute the command as an administrator. 
```
For mac users,  
``` bash
    brew install tree
```
Then the command will be installed.  
To see the architecture of current directory,  
``` bash
    tree
```  
For work directory,  
``` bash
    tree work
```  
  
## *echo*: print any word  
This command is used to print any word.  
``` bash
    echo "practice"
```
  
## *>*: redirect
Using this character, you can store the output of some command to a file.  
``` bash
    echo "practice" > test1
    ls          #You will find the "test1" file.
```  

## *cat*: print the content of files  
``` bash
    cat test1   #You can see the content of "test1" and confirm your command above has succeeded.
```  
`cat` can also be used for merge 2 files.  
``` bash
    echo "Linux" > test2
    ls          #You will find "test1" and "test2"
    cat test1 test2         #Now test1 and test2 are merged!
    cat test1 test2 > test_merge    #You can also store the merged output as files.
```  

## *less*: browse the file contents  
`less` command is used to read the file content. This command open a new window to read the file, so it's useful for browsing a large file.  
``` bash
    less test_merge #To quit browsing, pless "q".
```


