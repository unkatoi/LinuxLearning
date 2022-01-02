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
  
  


  
  

