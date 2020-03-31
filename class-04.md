## What is RegExr?
- RegExr is an online tool to learn, build, & test Regular Expressions (RegEx / RegExp). Supports **JavaScript** & PHP/PCRE RegEx. Results update in **real-time** as you type.
-  RegExr is extremely useful in *extracting* information from any **text** by searching for one or more matches of a specific search pattern (i.e. a specific sequence of **ASCII** or **unicode characters**).
#### Some of basic topics
- **Anchors — ^ and $**  

        ^The  -----> matches any string that starts with (the) 
        end$  -----> matches a string that ends with (end) 
        ^The end$  -----> exact string match (starts and ends with The end)   
        roar -----> matches any string that has the text (roar) in it
- **Quantifiers — * + ? and {}**

            abc*       ----->  matches a string that has ab followed by zero or more c 
            abc+       ----->  matches a string that has ab followed by one or more c
            abc?       ----->  matches a string that has ab followed by zero or one c
            abc{2}     ----->  matches a string that has ab followed by 2 c
            abc{2,}    ----->  matches a string that has ab followed by 2 or more c
            abc{2,5}   ----->  matches a string that has ab followed by 2 up to 5 c
            a(bc)*     ----->  matches a string that has a followed by zero or more copies of the sequence bc
            a(bc){2,5} ----->  matches a string that has a followed by 2 up to 5 copies of the sequence bc



**OR operator — | or []**

        a(b|c) ----->  matches a string that has a followed by b or c (and captures b or c) -> Try it!
        a[bc]  ----->  same as previous, but without capturing b or c   

**Character classes — \d \w \s and .**

        \d   ----->  matches a single character that is a digit -> Try it!
        \w   ----->  matches a word character (alphanumeric character plus

## grid
-  **What is CSS grid used for?**
- CSS *Grid Layout *is a **two-dimensional** grid-based layout system that aims to do nothing less than completely change the way we design grid-based user interfaces.
-  THE :*float, display: inline-block, display: table-cell, v  ertical-align and column-* properties have **no effect on a grid item.**
- One of the Properties for the Grid Container (the Parent) is  :
- **display**   
  - Defines the element as a grid container and establishes a new grid formatting context for its contents.

  - *Values*:
            
            grid – generates a block-level grid
            inline-grid – generates an inline-level grid

- **grid-template-columns**
  - Defines the columns and rows of the grid with a space-separated list of values.     
   - *Values*:

            <track-size> – can be a length, a percentage, or a fraction of the free space in the grid (using the fr unit)
            <line-name> – an arbitrary name of your choosing

grid-template-rows
- Of the Properties for the Grid Items (the Children) :

        grid-column-start
        grid-column-end
        grid-row-start
        grid-row-end

