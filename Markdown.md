# Contents

>  If you want to check the file behind the scenes either click on `<>` or `Raw` button on top-right corner

- [Heading `#`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#-character)

- [Font `*` or `_`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#the--or-_-characters)

- [Important notes](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#notes)

- [Quoting `>`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#the--character)

- [Lists:](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#lists)

   - [Unordered `-` `+`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#unordered-lists)

   - [Ordered `1. `](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#ordered-lists)

   - [Task `- [ ] `](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#task-lists)
   
- [Links:](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#links)
   
   - [Basic link usage `[]()` or `<url>`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#links) 
   
   - [Images `<>` or `![]()` or html](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#images) 
   
   - [Footnote `[^1]`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#footnotes) 
   
- [Adding Code **\` or \`\`\`**](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#adding-code) 

- [Adding a line `---` or `***` or `___`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#adding-lines)

- [Disabling a markdown character `\`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#disabling-a-markdown-character)

- [Using emoji `:Emoji code:`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#using-emoji)

- [Tables `|  |  |`](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#tables)

# Syntax

## **'#'** character: 

   - ### This character is used to create a heading **the more '#' you add the smaller it gets**
   
        - #### Name + Number of '#'
        
        - # Title1
        
            - ## Title2    
            
                - ### Title3
                
                    - #### Title4
                    
                        - ##### Title5
                        
                            - ###### Title6   
                            
                            > Note: cannot do the following: `####### Title7`. Since the maximum number is 6.
                            >
                            > That's how the title is done: `# Heading`

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

## The '*' or '_' characters: 

   ### Both of these characters have the same usage which is the following:

   1. Can be used for *italic* text format which is done as follows:

          *Italic* 
              
   - OR

         _Italic_
              
        - In each case the result is _Italic_
        
        -      -      -      -
        
   2. Can be used for **bold** text format which is done as follows:

          **Bold** 
              
   - OR

         __Bold__
              
   - In each case the result is __Italic__

        - - - - -

   3. Can be used for ***Bold + Italic*** text format which is done as follows:

          ***Bold + Italic*** 
              
   - OR

         ___Bold + Italic___
              
   - In each case the result is ___Bold + Italic___

        ----
        
   4. Can be used for **All Bold + Part _Italic_** text format which is done as follows:

          **All Bold + Part _Italic_** 
              
   - OR

         __All Bold + Part *Italic*__
                
   - OR

         **All Bold + Part *Italic*** / __All Bold + Part _Italic___
              
   - In each case the result is __All Bold + Part *Italic*__

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

### Notes: 

   > 1. It's recommended to use `*` instead of `_` . However, there are exceptions such as the number 4 above.
   >
   > 2. In order to write one new line you just have to press the `enter` or `return` key on your keyboard **twice**.
   > So that there is a blank line in between.
   >                       
   >        First line
   >
   >        Second line
   >       
   > 3. It's also recommended to use a blanked line in between each new line even if there is a special character that does a new line for you
   >
   >   **Example:**
   >
   >       1. First line
   >       2. Second line
   >
   >   Has the same result as the one bellow:
   >       
   >       1. First line
   >
   >       2. Second line
   >
   >   Result:
   >
   >   1. First line
   >   2. Second line
   >
   >   However, it's better to use the one with a blank in between. Since, it's more organized than the first.
   >
   > 4. Also add a space after using a special character. Moreover, if you run out of space in one line press enter`enter` or `return` key on
   >  your keyboard **once**, so it will remain on one line on the observer's view.
   >
   >   Example:
   >
   >           Some long text Some long text Some long text Some long text Some long text 
   >           Some long text Some long text Some long text Some long text Some long text 
   >           Some long text Some long text Some long text Some long text Some long text 
   >           Some long text Some long text Some long text Some long text Some long text 
   >   
   >   Results in: 
   >   
   >   Some long text Some long text Some long text Some long text Some long text 
   >   Some long text Some long text Some long text Some long text Some long text 
   >   Some long text Some long text Some long text Some long text Some long text 
   >   Some long text Some long text Some long text Some long text Some long text 

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

## The '>' character: 

   ### The character is used at the begining of a line similar to the #. It is used to write a quote or a note. I've used it to write the notes above.

   Example for basic usage: 

      > A note.

   **Result:**

   > A note.

   The text **remains on one line** if you type the following:  
      
      > Row1
      > Row2
      > Row3
   
   **Result:**
   
   > Row1
   > Row2
   > Row3

   As for **Multi-line text** is done as the following: 

     > First
     >
     > Second

   **Result:**

   > First
   >
   > Second 

   It can also be **nested** which means **one inside the other** like this: 

      > Main
      >
      >  > Sub
      >  >  
      >  >  > Sub-Sub..
   
   **Result:** 

   > Main
   >
   >  > Sub
   >  >  
   >  >  > Sub-Sub..

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

----------------------------------------------------

## Lists:
   
  > ### There are few types of lists that will be covered.
  >
  > ### Both of the *ordered* & *unordered* lists can be nested. You Could also **mix** between them and other characters that precede lines such as `#`, `>`.
   
   ### Unordered lists: 
      
   They are lists that have no specific arrangement. Each line is 
   preceded with one of the following characters `*`, `-`, `+`. 

   > Note: You should use one of these characters without mixing between them
   > for **consistency**.

   **Example:** 

      - This
      is an

      - Example.
   
   **Result:** 

   - This 
   is an

   - Example.

   ***OR*** 

      - This
      is an
      - Example.

   Here there is a difference in the output the 2 items **are closer** to each
   other: 
   
   - This
   is an
   - Example.

   **Nested** example:
       
       - Main

          - Sub

             - Sub-2

                - Sub-3..

   **Result:** 

   - Main

      - Sub

         - Sub-2

            - Sub-3..
   
   **Mixing** things up:

       - ##### Small
        
       - > ##### Small ***Quote***.
         >  
       - >   > 1. One.
         >  
       - >   > 2. Two.

       - > Another.

   **Result:** 

   - ##### Small
        
   - > ##### Small ***Quote***.
     >  
   - >   > 1. One.
     >   >  
   - >   > 2. Two.

   - > Another.

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

   ### Ordered lists: 
   
   This type of list is arranged using numbers (ordered). Each line is 
   preceded with a number with a dot and a space after e.g. `1. `.
   
   **Basic example:**
   
      1. First.
      
      2. Second
      
      3. Third
      
   **Result:**
   
   1. First.
      
   2. Second
      
   3. Third
   
   ***OR if you want to make the rows closer to each other:***
   
      1. First.
      2. Second
      3. Third
      
   **Result:**
   
   1. First.
   2. Second
   3. Third

   Some useful feature might be having the ability to still make an ordered list **without the need for 
   knowing the exact number** of items in that list:
   
      1. One
      
      1. Smth
      
      1. More
      
      1. Something else.
   
   **Result:**
   
   1. One
      
   1. Smth
      
   1. More
      
   1. Something else.

   > ***Note:*** The above example will work also if you provide **unordered numbers while the first number is `1. `**
   >
   > **Example:**
   >
   >     1. A
   >    
   >     9. B
   >    
   >     10. C
   >     
   > **Result:**
   > 1. A
   >    
   > 9. B
   >    
   > 10. C
   > 
   > Even so you still should not use random numbers since they will appear random while editing the file.

   ***It's also possible to start from another number than 1 just type it in the first row:***
   
      100. qwe
      
      101. asd
      
      102. zxc
      
   **Result:**
   
   100. qwe
      
   101. asd
      
   102. zxc

   You could also ***nesting*** and ***mixing*** just like **unordered list**.
   
[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

   ### Task lists:
   
   This type of list as the name suggests is used for mentioning tasks that you're going to do or that you've already done.
   you start by typing one of these characters `-`, `+`, `*` followed by `[ ]` Then a space and write the task.
   
   > For tasks that are still in porcess you do this `- [ ] ` there is a space between the square brackets which outputs :white_large_square:
   > For tasks that have been done you do this `- [x] ` type an x between the square brackets which outputs :ballot_box_with_check:
   
   **Example:**
      
      - [ ] Do that thing
      
      - [x] Write this down
   
   **Result:**
   
   - [ ] Do that thing
      
   - [x] Write this down

   Here too you can ***mix*** many characters together just like in the following **example:**
   
      ### - [ ] Do the following:
   
      > - [x] Create a repository.
      >
      > - [x] Add a sources file.
      >   
      >   > - [ ] Finish the file
      >   
      >   > - [ ] Updates   
      
   **Result:**
   
   ### - [ ] Do the following:
   
   > - [x] Create a repository.
   >
   > - [x] Add a sources file.
   >   
   >   > - [ ] Finish the file
   >   
   >   > - [ ] Updates   

   Notice there is not a checkbox on the first line. It seeems that there it's not possible to make a heading with a checkbox.
   
[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)
   
--------------------
   
## Links:
   
   > #### Links can be used for various purposes which will be mentioned in this section.
   > #### They are usually implimented by the following `[sometext](link)`

   ### Link usage:
   
   Links are created by typing **text between `[ ]`** which represents what's the link is about, 
   **followed by parentheses `( )`** that contain the **url**. There isn't a space between `[ ]` and `( )`.
   
   **Example:**
   
      [url meaning](https://support.google.com/google-ads/answer/14095?hl=en)
      
   **Result:**
   
   [url meaning](https://support.google.com/google-ads/answer/14095?hl=en)
   
   You can also mention the **url it self** between `<>` to make it a **link** as bellow:
   
      <https://support.google.com/google-ads/answer/14095?hl=en>
      
   **Result:**
   
   <https://support.google.com/google-ads/answer/14095?hl=en>
   
   You can format the link using Italic and/or bold like `*[this](url)*` or `[*this*](url)`
   
   Regarding how I done the [contents link](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents) 
   it's done as the following: 
      
      [contents link](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)
                                                                                                            
      [contents link](https://github.com/GithubDisplayName/RepositoryName/blob/main(BranchName)/FileName.Type#HeadingName)
      
   This information is useful to know especially when you are working with multiple branches on github or desktop with git
   and you are refering to some file in a **temporary branch** and after finishing your work on it you'll most likely want to
   **merge** the temporary branch with your main branch. When this happens the temporary branch is deleted and the link that 
   you provided stops working or **sends you to Not Found 404 page**. You'll need to **change the branch name in the link**.
   
   An easier way to make a link that sends the viewer to a specific heading in your markdown file is to:
   
   1. Open that file in Github.
   
   2. Go to the wanted heading.
   
   3. Hover over the heading (put the mouse's cursor/ pointer on the heading).
   
   4. You'll find this :link: sign on the left of the heading.
   
   5. If you press on it (left mouse click) you'll find that the url has changed.
   
   6. Copy the url and that's it.  
   
   > In heading part of url or any other part that includes names this is true:
   > 
   > - Spaces are replaced with `-`.
   > 
   > - Capital letters are replaced with small, e.g. `Contents` -> `contents`.
   > 
   > - Specific characters are omitted(removed) or replaced with `-`. Such as `*`, `#`, `:`, `>`, `<` ..

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

   --------------------
   
   ### Images 
   
   #### Another usage of links is providing images to which is done as the following: 
   ```
   ![name](url of image)
   ```
   **Example:**
   
      ![Mouse pointer](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png)
      
   **Result:**
   
   ![Mouse pointer](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png)
   
   If you want a title to appear on the image when hovering the mouse's pointer over it do the following: 
   
      ![Mouse pointer](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png "Pointer")
   
   **Result:**
   
   ![Mouse pointer](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png "Pointer")
   
   To add a link to an image when clicking on the image do the following: 
      
      [[Some Image name](Image url)](Some url to a website)
      
   **Example:**
      
      [![Mouse pointer](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png "Pointer (This is optional)")](https://www.google.com/search?q=what+is+the+mouse+arrow+called&client=firefox-b-e&tbm=isch&source=iu&ictx=1&fir=jLqywEM-DuRyoM%252CYR2K7DauKOD0vM%252C_&vet=1&usg=AI4_-kTSXhmbHAp1DFd1SJvhXy100CvjCg&sa=X&ved=2ahUKEwizn7LG_4b1AhURNOwKHbQkA54Q9QF6BAgTEAE&biw=1920&bih=940&dpr=1)
   
   **Result:**
   
   [![Mouse pointer](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png "Pointer (This is optional)")](https://www.google.com/search?q=what+is+the+mouse+arrow+called&client=firefox-b-e&tbm=isch&source=iu&ictx=1&fir=jLqywEM-DuRyoM%252CYR2K7DauKOD0vM%252C_&vet=1&usg=AI4_-kTSXhmbHAp1DFd1SJvhXy100CvjCg&sa=X&ved=2ahUKEwizn7LG_4b1AhURNOwKHbQkA54Q9QF6BAgTEAE&biw=1920&bih=940&dpr=1)
   
   Resizing images and aligning them in markdown is not possible with a special syntax however it can still be done using
   html as the following: 
   
   If you only need to resize an image while maintaing the original proportions: 
   
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png"
      style="width: 10%; height: 10%;"/>
      
   **Results:**
   
   <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png"
      style="width: 10%; height: 10%;"/>
      
   If you need to align the image to center/right/left do the following:
   
      <p align="center" >
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png" 
         style="width: 10%; height: 10%;"/>
      </p>
       
   **Results:**
   
   <p align="center" >
   <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Mouse-cursor-hand-pointer.svg/220px-Mouse-cursor-hand-pointer.svg.png" 
        style="width: 10%; height: 10%;"/>
   </p>
   
[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)   
  
   -------------------
   
   ## Footnotes
   
   #### They are not exactly links. However, they're similar to link in a way because they send you to a specific location
   #### in the file where you assigned the footnote.
   
   **Example:**
   
      Words of the day conspicious[^1] vivid[^1]
      
      lines...
      
      [^1]: is an adjective that describes something that clear or evident
      
   **Result:**
   
   Words of the day conspicious[^1] vivid[^1]
      
   lines...
      
   [^1]: is an adjective that describes something that clear or evident
   
   As you see the word you type a footnote is followed by `[^number of footnote]` **without a space between them**.
   Also the footnote it self is written wherever you need it like this `[^number of footnote]: `. However, the footnote 
   will appear at the end of your markdown file.
   
[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)   
   
   ----------------

## Adding code
   
   #### It's done using the following symbol **\`** like the following:
   
      `command x`
      
   **Result:**
   
   `command x`
   
   You could also type multiple lines of code with the following:
   
      ```
      line1
      
      line2
      
      line3
      ```
   
   **Result:**
   
   ```
   line1
      
   line2
      
   line3
   ```
   
   If you're writing in a specific programming language you could do this:
   
      ```C#
      System.Console.WriteLine("Hello, world");
      ```
   
   **Result:**
   
   ```C#
   System.Console.WriteLine("Hello, world");
   ```
   > To know more about the name to use following the triple \` check this <https://docs.github.com/en/github/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks>. Or check [this](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml) for specific name I recommend using `Ctrl+F` to search for the language you are looking for with a match case search (where C is different from c).
   >
   > The \` character is found on the top-left corner of your keyboard downward from `Esc`.

   The final method to do a block of code is using a tab on github or 4 spaces:
   
   ```
      line1
      
      line2
      
      line3

   ```
   
   **Result:**
   
      line1
      
      line2
      
      line3
   
   > I've noticed while working on this file that to make a line and a table in a code block using the `tab` 
   > might not work and for it to work use 4 spaces (1 `tab` and 1 `space`) it might work for you with one tab.
   
   -----------------

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

## Adding lines

Lines are added by using a consecutive order of characters which are `-`, `*`, `_`. I prefer to use `-` character consecutively as the following:

   `-----------------`
   
However, you could also use this:
   
    ---
   
    ***
   
    ___

**Result:**

---
   
***
   
___

> ## Disabling a markdown character
>
> To do that you simply add a back-slash `\` character before the markdown character like this:
>
> ```
> \* \- \+ \` \_ \# \> \*\*\*
> ```
>
> Result: \* \- \+ \` \_ \# \> \*\*\*

> ## Using emoji
>
> You can add an emoji to your markdown file like this `:Emoji code:`
>
> To find the emoji code you are looking for check the following [link](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)
> the link provides emoji tables.

---

[Back to contents](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#contents)

## Tables

To add a table you do the following: 

    |   num   |  name   |
    | ------- | ------- |
    |    1    |  Jason  |
    |    2    |  Jack   |
    |    3    |  Cherry |
   
**Result:**

|   num   |  name   |
| ------- | ------- |
|    1    |  Jason  |
|    2    |  Jack   |
|    3    |  Cherry |

I've notice that you can't use one of the characters that precede the line such as `#`, `-`, `>`.
However, if I find out otherwise I'll edit this.

There is also a **right-aligned column table** which is done like this:

    |   num   |  name   |
    | -------: | -------: |
    |    1    |  Jason  |
    |    2    |  Jack   |
    |    3    |  Cherry |

**Result:**

|   num   |  name   |
| -------: | -------: |
|    1    |  Jason  |
|    2    |  Jack   |
|    3    |  Cherry |

# That's it for this markdown file if find anything new worth mentioning I'll add it.
# [Back to LinuxLearning Repository](https://github.com/unkatoi/LinuxLearning)
