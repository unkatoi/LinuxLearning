# Contents

- [#](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#-character)

- [* or _](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#the--or-_-characters)

- [Important notes](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#notes)

- [>](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#the--character)

- [Lists:](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#lists)

   - [Unordered](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#unordered-lists)

   - [Ordered](https://github.com/unkatoi/LinuxLearning/blob/main/Markdown.md#ordered-lists)
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


<!--div style="text-align: center;">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Tux.svg/1200px-Tux.svg.png" style="width: 10%; height: 10%;"/>
</div-->

