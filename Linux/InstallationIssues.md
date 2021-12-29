# Installation issuses

- [boot menu keys e.g.`esc`, `F12`, `F9`](https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Linux/InstallationIssues.md#1-problem)

- [usb not showing up in boot menu](https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Linux/InstallationIssues.md#2-problem)

- [Before linux installation BIOS settings changes](https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Linux/InstallationIssues.md#3-problem)

- [Problem black screen OR repeated login screen](https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Linux/InstallationIssues.md#4-problem)

   - [printk messages OR Journal Service error](https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Linux/InstallationIssues.md#1-something-like-systemd1-failed-to-start-journal-service-or-printk-messages-dropped)

   - [No space left on device error](https://github.com/unkatoi/LinuxLearning/blob/LinuxFolder/Linux/InstallationIssues.md#2-failed-to-write-or-no-space-left-on-device-error-showed-up-while-following-videoes)

---


### In this file I'll be mentioning issuses that I've faced while or after installing a 
### linux distribution. 

### **This is not a guide for installing a linux distribution**.

## 

### While following a guide on how to install a specific linux distribution alongside with a windows 
### operating system on my computer. *Since, I've already had windows on the  device and didn't want* 
### *delete the operating system*. I've **encountered few problems**:

> After installing the linux distribution on a usb and making enough space for linux operating system.


### **1. Problem:**

-  The guide mentioned that I have to press a key on my keyboard while restarting the computer
  which will then take me to something called **boot menu** **(which basically is the menu for**
  **choosing what operating system you want to run such as `Windows`, `MacOS`, `GNU/Linux`)**.
  However the key did not work. 
  
  **Solutions:** 

  - Therefore I had to find it from the following link <https://www.disk-image.com/faq-bootmenu.htm>. 
    In addition, for **some computers you have to click on that key multiple times consecutively for it to work**.

  - Another way is to enter something called the **BIOS settings** which is basically responsible
    for running your operating system when you press the power button. This video shows you **how**
    **to get there if you did not find the key for boot menu works for _windows only_** <https://youtu.be/HQXFd0CN4s8>


### **2. Problem:**

- The guide mentioned to I have to plug in the **usb before restarting the computer**. However, 
  that did not work. Because, the usb did not show up on boot options menu.

  **Solution:**

  - **After you've reached** a black screen with a white **`Startup Menu` title** using the **boot menu key** 
    plug in the usb and wait few seconds, then press the key that shows up next to `Boot Device Options`. 
    And you should find your usb on the list.
    

### **3. Problem:** 

- The guide did not mention that there are **specific BIOS settings that need to be modified** in order
  to install the linux distribution.

  **Solution:**

  - Go to settings and then to **boot** options (in the menu) **disable secure-boot** and **enable `Legacy` mode/boot**. 
    The **interface** (how it looks/designed) of **BIOS depends entirely on the manufacturer** so I can't specify how
    to do that exactly, but **there should be a list of keys** that explains what each key does at the **bottom of your screen**.

  - Go to `security` from the menu and look for **`TPM Device` make it available**  and then you will find **`TPM State`** 
    **and change it to `Disabled`**.

  - If **after you've done the above** still **did not work to install**, then go to **`Advanced` and change** 
   **`Virtualization Techology` to `Enabled`**


### **4. Problem:**

- I've found myself on a **black screen during the installation** process (in the middle of installing the OS) OR
  when I **turned on the computer** to use linux OR a **tty1 showed up `DistroName GNU/Linux Rolling DistroName tty1`**
  and asked to login

**Solutions:** 

- use `Ctrl+Alt+F1` or you could change f1 up to f6 which basically open up a new command line interface with some 
  message asking you to login like tty1 up to tty6. From there follow instructions from videoes or websites
  that explain how to fix tty1 or whatever shows on your screen. For example the following [video](https://youtu.be/KcB6H3U7GQQ)
  or search [StackExchange](https://superuser.com/questions/65185/when-i-start-ubuntu-it-enters-tty1-6-instead-of-my-desktop-how-do-i-get-to-de)
  I think that you should try these and if they did not work try other things.

### **Important:** while trying some solutions from numerous websites and videos I stumbled upon **more errors**:

#### 1. Something like **`systemd[1]: Failed to start Journal Service.` or printk messages dropped.** 
#### This error **sometimes doesn't let you write down commands** in order to fix the main problem (tty1).

**Solution?** 

Well for this specific problem I tried numerous things that did not solve the problem. But after turning on
the computer in the next day it's fixed. What I've done is:
    
- Change the **BIOS settings like I mentioned above**.

- Used `Num Lock` on the keyboard where 8 goes up a row 2 down a row and started typing text where the Error was
  written then deleted it (with :arrow_left: key) and continued to write commands

- Tried to **write the necessary commands to fix tty1 before these errors start to show up**
 
   1. Turn off the computer.
      
   2. Open it up again with windows.
      
   3. Then press restart.

   4. Enter boot menu and choose Linux.

   5. use commands to fix tty1..

#### 2. `Failed to write` OR `No space left on device` error showed up while following videoes
#### on how to fix tty1.

**Solution:**

1. Fisrt use the following command: `sudo df -h` which will show you the size of your
   partitions and how much is `Used` and how much is `Avail` (available) to find out 
   which one is full.

2. Use the following command: `sudo du -ah | sort -hr | head -10` which sorts the files 
   that are inside your current directory and starts by showing you the top 10  
   largest files with how much GB might show up `G` or `M` (MB) or `K` (KB)

3. If step 2 doesn't work for some reason try this command `sudo du -h --max-depth=1 /FolderName` 
   What this command do is list files and folders that are available in the given folder without 
   sorting from high to low space usage Which might require time to find the largest file.
   **If you don't use this command you can go to step 4 since it mentions the files that might**
   **be the largest**

4. Use sudo rm and the largest filename as it is shown in the list. **Be caureful not to** 
   **delete another file**. 
           
   As for the question is **it okay to delete it?**

   First you should **check for the file in the internet** and you should find answers.
   If not, then **if the file is larger than 10 GB** then I think that it's okay delete
   it. **Since the entire linux operating system requires 10-20 GB And won't be all in**
   **one file.** 

   There are **3 files that might be the files that take up all your space which are:**
   **`/var/log/syslog`, `/var/log/messages`, `/var/log/kern.log`.**
   Each one of these 3 files took 77 GB after I deleted them the problem was fixed.

5. Check the **available space again like in step 1** if it's still full.
           
   1. Try the command `sudo df -h` 3 times  with one minute in between the computer
      might still deleting or processing the new available space.
           
   2. If it's still full then use this command `sudo lsof | grep deleted`, which 
      shows you the deleted files that the computer is currently using.
           
   3. Use this command `sudo killall Process Name` to force the computer not to 
      use the deleted files. Process Name is the name that appears on the list 
      from step 2 which is on the left side of the screen. However if you use 
      `kill` you would need PID (Process id which is the number right next to 
      process name)
              
      > The computer might decide to use deleted files after
      > you restart the computer. So you should check for the current available space
      > if you find the same error or the computer is slowing down and the steps again.

6. Check the **available space again like in step 1** if it's still full then try searching 
   the internet for more information.


    



