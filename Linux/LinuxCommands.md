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





