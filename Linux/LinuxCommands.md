# Linux commands (Bash Shell)

>  When something is written inside e.g. `<text>` **do not add the symbols <> when you type it** in the terminal. 
> Also the **text** doesn't work it **only explains what needs to instead of `<text>`**

## `whoami`

### This command prints the currently logged account's username.

## `man <command>`

### This command provides a manual page for the command that you've provided in place of `<command>`.

### In order to leave the manual page you press `q`.

### You can scroll through the manual page with up/down arrow.

### For faster scrolling you could press space.

## `clear`

### This command clears all the previous commands that you've run in the current terminal window.

### However, you can still find the history of your commands.

### Options:

- #### `-x`

  - **Usage:** The command is written then add the option like this: `clear -x`.
  
  - **Purpose:** The option enables scrolling back through the cleared commands
  (they're not removed like with normal `clear`).

> ### Options can be found in manual page using the `man` OR `--hlep` command.
  
## `pwd`

### This command prints full directory path for the directory (folder) that you're currently in.

### The command itself is an acronym for: Print Working Directory.

## `ls`

### Lists all the files and folders that are inside the current directory (the one that you are in).

### You can add a folder name that is inside your current directory. In order to list all the files and folders inside that directory. **Usage: `ls <directory(folder) name>`**.

### You can add **full path** to a directory(folder). In order to list all the files and folders inside that directory. **Usage: `ls <path>`**.

### Illustration: 

<p align="center" >
  <img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lsCommand.png" 
       style="width: 80%; height: 80%;"/>
</p>

### Options: 

- #### `-l`

  - **Usage:** `ls -l`.

  - **Purpose:** prints a long listing format as in the following illustration.
  
<p align="center" >
  <img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lsCommandOptionL.png" 
       style="width: 80%; height: 80%;"/>
</p>

  - **Example: `drwxr-xr-x 2 panda panda  4096 Jan  2 01:45 Linux`**

  **Explination:**

  - The **first character(`d` in example)** can represent a:

    - **File (if the first character is a `-`.)**

    - **Directory (if the first character is a `d`.)**

    - **Link (if the first character is a `l`.)**

  > In the **example** the first character is **`d` meaning it's a directory.**

  **Now will be deviding the next part into the following:**

  **Permissions:**

  - **`rwx`** - **The owner** has over the file. 

  - **`r-x`** - **The group** has over the file. 

  - **`r-x`** - **Everybody else** has over the file. 

  > **`r`** stands for **read**.
  >
  > **`w`** stands for **write**.
  >
  > **`x`** stands for **execute**.
  >
  > **`-`** stands for **not having that permission. e.g. `r-x` doesn't have permission to write**.

  - The next part from the example is `2`:

    It specifies the **number of files that contain links** or **number of directories inside this directory.**

  - The next part from the example is `panda`:

    The **user that owns the file or directory.**

  - The next part from the example is `panda` again:

    The **group that the file or directory belongs to.** Also any **user in that group** will have the following **permissions: `r-x`** (read & execute).

  - The next part from the example is `4096`:

    It's the **size (in bytes)** of the file or directory that is listed.

  - The next part from the example is `Jan  2 01:45`:

    The **date of last modification to the file or directory**. It is: `month day 24hour(time)`.
    
  > If years have passed since the last modification it will mention the year instead of time e.g. `Aug 21  2009`.

  - The next part from the example is `Linux`:

    The **name of the file or directory**.
    
- #### `-s`

  - **Usage:** `ls -s`.

  - **Purpose:** prints the size of each file in KB.

  **Illustration:**
  
<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lsCommandOptionSmallS.png"
  style="width: 80%; height: 80%;"/>
</p>

- #### `-h`

  - **Usage:** `ls -sh` OR `ls -lh` OR seperated options:`ls -l -h`.

  - **Purpose:** file **sizes become more readable** and faster to comprehend e.g. `1K`, `234M`, `2G`..

  > `K` stands for Kilobyte. `M` stands for Megabyte. `G` stands for Gigabyte.

- #### `-S`

  - **Usage:** `ls -S` OR combined with other options `ls -lSh`.

  - **Purpose:** **sort by file size**, **starting with largest** and ending with smallest.

  **Illustration:**
  
  <p align="center" >
  <img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lsCommandOptionS.png"
       style="width: 80%; height: 80%;"/>
  </p>
  
- #### `-a`

  - **Usage:** `ls -a` OR `ls --all`.

  - **Purpose:** doesn't ignore files/directories that start with a dot e.g. `..`. Meaning that it shows you hidden directories/files.

  **Illustration:**
  
  <p align="center" >
  <img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lsCommandOptionSmallA.png"
       style="width: 80%; height: 80%;"/>
  </p>

## `help <command>`

### The command is used to find out more **information about a shell command** e.g. `cd`.

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/helpCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

## `cd <directory>` OR `cd <path>`

### The command means **change directory**. Which is basically used to **go from the current directory(folder) to another.**  

### The **`~` directory is a shortcut for `/home/username`.**

### The **`..` directory refers to the previous directory.**

### The **`.`** directory refers to the **current directory**.

### The root directory(folder) is the starting point for the file system. It's called root and the actual directory name is `/`.

### The **home directory `/home`** contains a home folder for each user e.g. `~` is `/home/panda` 

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/cdCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

> As you can see in the example above. I've used **full path to the `SomeMiniFolder`**
> **directory which is `~/Desktop/SomeFolder/SomeMiniFolder/`**.
>
> In addition, I've used the following **`cd ..` in `/home/panda/LinuxLearning/Linux`** 
> directory and then it went back to the **parent directory which is `/home/panda/LinuxLearning`**.
> While the **`cd ../../..`** is basicly going to the **parent directory 3 times.**
>  It was used in **`~/Desktop/SomeFolder/SomeMiniFolder` directory then it went to `~` directory.**
>
> In order to **write** the directory **paths faster I use the `Tab`** on keyboard while in terminal.
>  What it does is **complete the directory(folder) name** if there is only **one possiblity to complete it** (that's when you press on the **`Tab` once**).
> However,  when you press on the **`Tab` twice** it will show you **all possible completions** like in the **example** above I pressed `Tab` twice and it showed me the following: 

```
bin/        dev/        lib/        libx32/     mnt/        root/       srv/        usr/        
boot/       etc/        lib32/      lost+found/ opt/        run/        sys/        var/        
.cache/     home/       lib64/      media/      proc/       sbin/       tmp/        

```

## `mkdir <directory name>`


### The command is used to **create a directory with the name that you provide**.

### The command is **short for make directory**.

**Example1:** creating **one directory** called SomeFolder `mkdir SomeFolder`.

**Example2:** creating **multiple directories** called dir1, dir2, dir3, dir4:

 `mkdir dir1 dir2 dir3 dir4`.

**Example2:** creating **nested directories** called Parent, Child, GrandChild:

`mkdir Parent`
`mkdir Parent/Child`
`mkdir Parent/Child/GrandChild`

> From Example2 notice that you can provide a **full path while creating a directory** e.g **`mkdir ~/Desktop/Parent/Child/GrandChild`**, (Assuming of course that `Parent` already exists in `Desktop` & `Child` already exists in `Parent`).

### Options: 

- #### `-p`

  - **Usage:** `mkdir -p`.

  - **Purpose:** Create **nested directories in one line (faster)**. Without the need for the directory being created before creating a directory inside it.

  - **Example:** creating **nested directories** called Parent, Child, GrandChild: **`mkdir -p Parent/Child/GrandChild`**.

## `touch <file name>`

### The command is mostly used to **create empty files**. Because,  when the **file** that you provide to the command **doesn't exist it creates it**. 

**Example:** `touch SomeText.txt` OR `touch SomeText` do the same thing. However, `touch SomeImage.png` here will be an empty `png` file.

**Example:** creating **multiple files at once** in the same directory: `touch file1 Img.png Doc.docx`.

### The main purpose of the `touch` command according to the manual page is to update the access and modification time of existing files that you provide with touch.

**Example:** when I use `ls -l ~/Desktop/SomeFolder` it shows me the following: **`drwxr-xr-x 2 panda panda 4096 Jan  3 23:52 SomeMiniFolder`.**

**After** I use: `touch ~/Desktop/SomeFolder/SomeMiniFolder/` it shows: **`drwxr-xr-x 2 panda panda 4096 Jan  4 23:48 SomeMiniFolder`**.

## `rmdir <directory name>`

### The command is used to **remove an empty directory**. And you can remove multiple directories by seperating them with spaces e.g. `rmdir dir1 dir2 dir3`. **Cannot delete directories that are not empty**.

## `rm <file name>`

### The command is used to remove files and directories. Be careful when using `rm` because the files and directories are **deleted in an instant and cannot be recovered**.

**Example:** you can delete multiple files at once `rm file1 Img.png Doc.docx`.

### Options: 

- #### `-v`

  - **Usage:** `rm -v <file/directory name>`.

  - **Purpose:** exaplains what is being done. Basically it **mentions which files or directories are being deleted** with the `rm` command. The option is also available in other command. you can also use it like this: `rm --verbose`.

  **Illustration:**
  
  <p align="center" >
  <img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/rmCommandOptionSmallV.png"
       style="width: 80%; height: 80%;"/>
  </p>
  
- #### `-r`

  - **Usage:** `rm -r <directory name>`.

  - **Purpose:** remove directories and their contents recursively. Which basically means to **delete an entire folder and everything inside** them. Also notice that this also happens **in an instant, thus BE CAREFUL**.

  - **Example:** `rm -r SomeFolder`.

- #### `-i`

  - **Usage:** `rm -i`.

  - **Purpose:** ask the user(you) **before deleting each file or folder** that you provided **if you want the file to be removed or not** (type `y` for deleting the specified file or type `n` for not deleting(keeping) the specified file).

  - **Example:** a directory`rm -ir SomeFolder` OR one file `rm -i AFile`.

- #### `-I`

  - **Usage:** `rm -I`.

  - **Purpose:** **Ask** the user **once every 3 files before deleting** any file if you want the file deleted or not.

  - **Example:** `rm -I SomeFolder`

- #### `-d`

  - **Usage:** `rm -d <Empty directory name>`.

  - **Purpose:** **Delete an empty directory** and it's used to make sure that you are **not deleting a directory that has contents in it** while at the same time give you the **capabiliy for deleting a directory**(because `rm` can't delete a directory without an option added to it). 

  - **Example:** `rm -d EmptyFolder`. As for `rm -d NotEmptyDir` this one gives an error.

  > Does the **same** thing **as `rmdir`**.

**Illustration:** For options combined

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/rmCommandOptionsIid.png"
     style="width: 80%; height: 80%;"/>
</p>

## `open <filename>`

### The command opens a file or a directory or an URL outside the terminal (A graphical interface pops up). 

### The command might not work for some linux distributions and would have to use `xdg-open` which is the actual command that exists in bash. 

**Example:** with `open`: 

`open someText.txt`, `open ADoc.docx`, `open https://www.duckduckgo.com`

Same but with `xdg-open`:

`xdg-open someText.txt`, `xdg-open ADoc.docx`, `xdg-open https://www.duckduckgo.com`

### If you don't have the command you can install it with `sudo apt install xdg-utils`

## `mv <file name> <optiona1: the file's new location OR option2 file's new name>`

### The command is used to **move files from** their **current location to another** OR  **rename a file**.

### Options: 

- #### `-v`

  - **Usage:** `mv -v <file name> <new name OR new location>`.

  - **Purpose:** exaplains what is being done. Basically it **mentions the file  that is being renamed or relocated** with the `mv` command.

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/mvCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

> ### As you see in the example above you can **move / rename multiple files** with one command as long you provide the path needed for the file.
> 
> I've also **tried using option -i** (interactive) however it **doesn't work** in case it does I might add it in the options above.

## `cp <name> <copy's name>`

### The command is used to copy files or directories into a new file or directory it can also be in a different location.

### Options: 

- #### `-r`

  - **Usage:** `cp -r <dir> <dir cp>`.

  - **Purpose:** **Copy the entire directory** including all the files and directories that it contains

- #### `-v`

  - **Usage:** `cp -v `.

  - **Purpose:** Explain what is being done. Check example

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/cpCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

### As you can see in the example you use the command as follows **`cp <name of a file> <the copy's name>`**. For **directories `cp -r <name of a dir> <the copy's name>`**.

### It's worth mentioning that you can Also add full path in case you want to c**hange the copy's file location** like I did above `cp -v FSCopyDir/F2/ ~/Desktop/`. Also the command **did not work** because F2 is a directory which you need to **add the `-r`** option for (in order to copy it).

## `head <file name>`

### The command **prints** in the terminal the **first ten(10) lines of the file** that you provide.

### Options: 

- #### `-n`

  - **Usage:** `head -n <N> <file name>`.

  - **Purpose:** **Prints the first N number** of lines that you provided in the command. e.g. **`head -n 50 LongText.txt`** prints the **first 50** lines from `LongText.txt` file into the terminal.
  
- #### `-v`

  - **Usage:** `head -v <file name>`.

  - **Purpose:** **Prints the file's name** before printing the first 10 lines that are inside the file. e.g. `==> README.md <== ` as you see bellow

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/headCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

## `tail <file name>`

### The command **prints** in the terminal the **last ten(10) lines of the file** that you provide.

### Options: 

- #### `-n`

  - **Usage:** `tail -n <N> <file name>`.

  - **Purpose:** **Prints the last N number** of lines that you provided in the command. e.g. **`tail -n 50 LongText.txt`** prints the **last 50** lines from `LongText.txt` file into the terminal.
  
- #### `-f`

  - **Usage:** `tail -f <file name>`.

  - **Purpose:** Doesn't stop reading from the file when it reaches the end of file. Instead it waits for additional data to be added to the file.

> ### For some reason this option **doesn't work on linux** but it does **work on macOS**. However, there is another **alternative which is `-F` option** which is similar but instead of adding new data to the end of file it **reprints the final 10 lines until you stop it with `Ctrl + C`**. Check example bellow

- #### `-v`

  - **Usage:** `tail -v <file name>`.

  - **Purpose:** **Prints the file's name** before printing the last 10 lines that are inside the file. e.g. `==> README.md <== ` as you see bellow

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/tailCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

**Illustration: `-F` before editing file** 

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/tailCommandOptionF.png"
     style="width: 100%; height: 100%;"/>
</p>

**Illustration: `-F` after editing file** 

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/tailCommandOptionF2.png"
     style="width: 100%; height: 100%;"/>
</p>

## `date`

### The command **prints the current date and time** e.g. `Fri 07 Jan 2022 20:24:24 UTC`. You can format the date to suit your needs check the format with `man date`

### Options: 

- #### `-u`

  - **Usage:** `date -u`.

  - **Purpose:** Print the date and time based on the universal clock.

## `<command> > <file location (inlcudes name)>`

### The is not exactly a command it's a redirecting standard output operator. What it basically does is take the **command's output** (text that the command on the left side prints) and **redirect** (instead of printing it into the terminal) it **into the file** (that you provide on the right side).

### **Important:** the operator **replaces everything** that is in the given file with the **command's output**. It **deletes file's contents then adds the command's output**.

## `<command> >> <file location (inlcudes name)>`

### It's a redirecting standard output operator similar to the earlier one. However, it **doesn't delete** the file's **contents** it **appends(adds) the command's output to the end of the file**. 

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/RedirectionOperators.png"
     style="width: 80%; height: 80%;"/>
</p>

> ### As you look at the image above you see that each time I use **`>`** operator the file's contents are **deleted**. However, when I use **`>>`** the contents are **added**.
> 
> For **both operators** if the **file doesn't exist it will create it** and continues the redirection of command's output to the new file.

## `cat <file name>`

### The main purpose of the command is to concatenate files. e.g. `cat File1 File2` prints everything inside the first file then the second file (at the same time no seperation between the files) onto the terminal.

### The command can print the entire file's contents. e.g. `cat AFile` prints everything inside it onto the terminal.

### Options: 

- #### `-n`

  - **Usage:** `cat -n <File name> <More files if needed>`.

  - **Purpose:** Prints line numbers on the left side of the line.
  
**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/catCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

## `less <file name>`

### The command opens the contents of a file inside a user interface similar to that of a manual page.

### In order to **scroll** through it you use:

-  **arrow keys(⬆️/⬇️)** for **one line up/down** at a time.

- **Space** for ***one page down*** at a time.

- **`B`** for ***one page up*** at a time.

- **`Shift + G`** for going to the **end of file**.

- **`G`** for going to the **begining of file**.

### In order to **search** for things inside that file you use: `/<what you want to search for>` while inside of the page.

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lessCommand1.png"
     style="width: 80%; height: 80%;"/>
</p>

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lessCommand2.png"
     style="width: 80%; height: 80%;"/>
</p>

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/lessCommand3.png"
     style="width: 80%; height: 80%;"/>
</p>

## `echo <text>`

### The command ***prints out whatever text you provide***. 

**Example:** `echo "This is some text"`

**Output:** This is some text

### It might be useful when you one to add a line for a file without the need to open it and edit.

**Example:** `echo "My repository name is LinuxLearning" >> GitInfo.txt`

**Output:** it's added to `GitInfo` file and if it doesn't exist it is created and then added the text *My repository name is LinuxLearning*.

### Options: 

- #### `-e`

  - **Usage:** `echo -e "Some text"`.

  - **Purpose:** The option provides more possiblities to modify text. For instance, you can add new lines while the text is written in one line e.g. `"First line.\n Second line"`. You can check what are the **escape sequences**  that can be used with this command **`man echo`**. 

**Example:** `echo -e "First line \tHere is a tab.\nNew line"`

**Output:**

```
First line      Here is a tab.
New line    
```

> Might change based on your tab e.g. mine is 5 spaces

## `wc <file name>`

### The command is a shortcut for word count. It prints the number of words, line, bytes of a file. Output is `lines words bytes <name of file>`

**Example:** `wc README.md`: 

`21  107 1057 README.md`

### Options: 

- #### `-l`

  - **Usage:** `wc -l <file name>`.

  - **Purpose:** prints only the **number of lines** . 

- #### `-w`

  - **Usage:** `wc -w <file name>`.

  - **Purpose:** prints only the **number of words** . 

- #### `-c`

  - **Usage:** `wc -c <file name>`.

  - **Purpose:** prints only the **number of bytes** . 

- #### `-m`

  - **Usage:** `wc -m <file name>`.

  - **Purpose:** prints only the **number of characters** (letters, numbers, symbols). 

### Piping:

### It's taking the *output of a command*  and pass it as an *input for another command*. 

### It's done using the `|` character. *`<command 1> | <command 2>`*.

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/wcCommandAndPiping.png"
     style="width: 80%; height: 80%;"/>
</p>

## `sort <file name>`

### The command sorts the file alphabetically (`A` -> `Z`) it's also case sensitive e.g. `S` is before `s`.

### If you have text on ***one line*** that you want it to be sorted it ***won't work*** it sorts only if the ***text is on seperate lines***.

### Options: 

- #### `-f`

  - **Usage:** `sort -f <file name>`.

  - **Purpose:** ignores the case of a letter (samll and capital letters are treated in the same way).

- #### `-n`

  - **Usage:** `sort -n <file name>`.

  - **Purpose:** sorts the numbers in an ascending order.

**Example:** `echo -e "100 \n90 \n95 \n89 \n91" | sort -n`

**Output:** 

```
89 
90 
91
95 
100 
```

- #### `-r`

  - **Usage:** `sort -r <file name>`.

  - **Purpose:** reverses the order from ascending to descending. 

**Example:** `echo -e "100 \n90 \n95 \n89 \n91" | sort -nr`

**Output:** 

```
100 
95 
91
90 
89 
```

- #### `-u`

  - **Usage:** `sort -u <file name>`.

  - **Purpose:** does not repeat the same numbers/words. Only unique text remains.

**Example:** `echo -e "90 \n100 \n90 \n95 \n89 \n91 \n90" | sort -nu`

**Output:** 

```
89 
90 
91 
95 
100
```

## `uniq <file name>`

### The command ***ignores consecutive repeated(adjacent[^1] matching lines)*** lines that contain the same text on them, displaying only unique text.

[^1]: lines that are close to each other.

### The command is used ***more efficently with `sort`*** since it gathers all the matching lines next to each other and uniq can remove the duplicates.
### Options: 

- #### `-u`

  - **Usage:** `uniq -u`.

  - **Purpose:** The option displays only unique lines. Lines that are not repeated consecutively(adjacent[^1] matching lines).

  > Notice the picture down bellow ends with `uniq -u`. 
  > The `option1` that was repeated 3 times in a row 
  > was omitted completely in the result, however duplicates on non-adjacent[^1] lines remain

- #### `-i`

  - **Usage:** `uniq -i`.

  - **Purpose:** The option ignores the case of the letter treats `S` or `s` the same.

  > Notice the picture down bellow ends with `uniq -i`. 
  > When I added `Option1` to the echo command it ignored the case `Option1` is same as `option1` that was before it.
  >
  > However, this time when I changed case again it considered it to be a different word. That is why it **shows at the end `option1` twice**.

- #### `-d`

  - **Usage:** `uniq -d`.

  - **Purpose:** The option displays only duplicate/repeated(non-unique) lines. Lines that are repeated consecutively(adjacent[^1] matching lines).

  > Notice the picture down bellow ends with `uniq -d`.
  > 
  > The command printed `option1` that occurred 3 times without mentioning the `option1` that occurred twice. That might be because the exact same text cannot be mentioned more than once when it's displaying duplicates. 

- #### `-c`

  - **Usage:** `uniq -c`.

  - **Purpose:** The option displays the number of occurrences(how many times a line was repeated) before displaying the line itself.

  > Notice the picture down bellow ends with `uniq -c`.
  >
  > As you see the number of each repetition is displayed on the left side.

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/uniqCommand.png"
     style="width: 80%; height: 80%;"/>
</p>

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/uniqCommandSort.png"
     style="width: 80%; height: 80%;"/>
</p>

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/uniqCommandSortPiping.png"
     style="width: 80%; height: 80%;"/>
</p>

## Expansion

### Giving a symbol another meaning similar to using a shortcut where `rm` is replaced with `remove`. It's also similar to a variable where a specific name represents a value. e.g. `~` is varries from user to another since it's `/home/username`.

### Symbols:

#### `$<variable name>` it refers to the value that a variable holds. Check example bellow:

**Illustration:**

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/ExpansionsDollar.png"
     style="width: percentage%; height: percentage%;"/>
</p>

> The variable name comes right after the `$` as shown in the image `USER` is the username there are other variables that might be added when I find them.

#### `*` it refers to every path in the current directory(folder). Check example bellow:

#### `?` it refers to any character that holds that specific place. Check example bellow:

#### `{<comma seperated values>}` it seperates all the values given. e.g. `value1 value2 value3`. Check example bellow:

**Illustration:**

| Color | Representation |
| -----  | ----------- |
| **Green** | Something **constant** (that doesn't change) doesn't include Expansion |
| **Blue** | What the **`*`** represents|
| **Red** | What the `?` represents |

> As you see the **`*`** in the first line refers to any **text that comes at any length**. `*` can be `Linux`, `Markdown.md`, `README.md` ..
> 
> The **`??`** in the second command it represents any **one character** t

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/ExpansionsNoDollarPart1.png"
     style="width: percentage%; height: percentage%;"/>
</p>

<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/ExpansionsNoDollarPart2.png"
     style="width: percentage%; height: percentage%;"/>
</p>

**Illustration:**

> You **cannot add spaces between the comma seperated values** as you see in the output of the first command it creates something that was not intended e.g. `App.{cs`, `csproj,` ..
>
> However, when I **do not add spaces** in the **second command** it created the **files called `App`** but with a **different type** one is `cs` (programming language C#) `txt`..


<p align="center" >
<img src="https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Pictures/ExpansionCurlyBrackets.png"
     style="width: percentage%; height: percentage%;"/>
</p>

