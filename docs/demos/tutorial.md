# A Brief Overview Of Markdown

Due to the variety of extensions installed, this site has a specific flavor of markdown in use. This document shows every possible markdown element, and the syntax to produce it.

## Headings

```markdown
## Heading 1

### Heading 2

#### Heading 3

##### Heading 4

###### Heading 5
```
## Heading 1

### Heading 2

#### Heading 3

##### Heading 4

###### Heading 5
    
## Inline Markup

### Basic Formatting

```
This is some prose. 
You can format text as **bold**, *italic*, 
_italic (alternative)_, ~~strikethrough~~, `code`, 
^superscript^ or ~subscript~.
```

This is some prose. 
You can format text as **bold**, *italic*, 
_italic (alternative)_, ~~strikethrough~~, `code`, 
^superscript^ or ~subscript~.
    
### Links
```markdown
Add a plain link (<https://google.com>) or an 
[inline link](https://www.chiefdelphi.com).

Link to other files within the documentation, 
such as the [home page](../index.md). Links are resolved relative
to the directory of their containing file.

Link to sections within the page: [Heading Examples](#headings)
```
Add a plain link (<https://google.com>) or an [inline link](https://www.chiefdelphi.com).

You can additionally link to other files within the documentation, 
such as the [home page](../index.md). Links are resolved relative
to the directory of their containing file.
 
Link to sections within the page: [Heading Examples](#headings)
    
### Syntax Highlighting
```markdown
You can add syntax highlighting to inline code by 
specifying the language: `:::java double f = 1023 / velocity;`
```

You can add syntax highlighting to inline code by 
specifying the language: `:::java double f = 1023 / velocity;`
    
### Math
```markdown
Inline equations using TeX syntax: $a^2 + b^2 = c^2$ 
```
Inline equations using TeX syntax: $a^2 + b^2 = c^2$ 

### Keys

    You can insert formatted key combinations.

    ++ctrl+alt+delete++
    
    ++cmd+tab++
    
    Press ++bracket-left+bracket-right+backslash++ to enable your robot.
    
    You can insert custom text: 
    
    It's a good idea to bind straight forward and straight backward to 
    ++"RT"++ and ++"LT"++ on your controller.


You can insert formatted key combinations.
    
++ctrl+alt+delete++

++cmd+tab++

Press ++bracket-left+bracket-right+backslash++ to enable your robot.

You can insert custom text: 

It's a good idea to bind straight forward and straight backward to 
++"RT"++ and ++"LT"++ on your controller.
    
A full list of key codes is avaiable [here](https://facelessuser.github.io/pymdown-extensions/extensions/keys/).


## Blocks

Block items such as code, blockquotes, or admonitions interrupt the paragraph and exist on their own line.

### Code Blocks

    Create generic code blocks:
    ```
    ./gradlew deploy
    ```

Create generic code blocks:
```
./gradlew deploy
```
---
    You can also create them by indenting with four spaces 
    (this is useful for nesting):
    
        ./gradlew deploy

You can also create them by indenting with four spaces 
(this is useful for nesting):

    ./gradlew deploy


#### Syntax Highlighting
    
        Specify a language to add syntax highlighting:
        
        ```python
        print "Hello world!"
        ```
    
    Specify a language to add syntax highlighting:
    
    ```python
    print "Hello world!"
    ```
    A list of supported languages is [here](http://pygments.org/languages/).

#### Highlighting Lines
    You can highlight specific lines to emphasize them.
    ```java hl_lines="3"
    public class Main {
      public static void main(String[] args) {
        System.out.println("Hello world!");
      }
    }
    ```
    
You can highlight specific lines to emphasize them.
```java hl_lines="3"
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello world!");
  }
}
```
---
    Multiple lines are space-seperated.
    
    ```python hl_lines="4 5"
    x = 1
    y = 2
    
    z = x + y
    print z
    ```
    
Multiple lines are space-seperated.

```python hl_lines="4 5"
x = 1
y = 2

z = x + y
print z
```

### Admonition Blocks

    !!! note 
        Create a separate box with contents.
    
    !!! info
        Blocks can contain multiple paragraphs.
        
        They can also contain other elements like code:
        ```python
        print "Hello, world!"
        ```
        
        !!! tip 
            They can even contain other blocks!
 
!!! note 
    Create a separate box with contents.

!!! info
    Blocks can contain multiple paragraphs.
    
    They can also contain other elements like code:
    ```python
    print "Hello, world!"
    ```
    
    !!! tip 
        They can even contain other blocks!

#### Titles
    !!! note "Blocks can have custom titles."
        The identifier just determines the icon and color.
    
    !!! note ""
        You can omit the title entirely.
        
    !!! note "Or have just the title."
    
!!! note "Blocks can have custom titles."
    The identifier just determines the icon and color.

!!! note ""
    You can omit the title entirely.
    
!!! note "Or have just the title."

#### Details
    Create detail blocks by replacing `!!!` with `???`.
    
    ??? question "What happens when I click on a detail block?"
        It opens!
    
Create detail blocks by replacing `!!!` with `???`.

??? question "What happens when I click on a detail block?"
    It opens!

---

    You can also make blocks expanded by default with a `+`.
    
    ???+ tip
        Use Admonition and Detail blocks for all sorts of information.
    
You can also make blocks expanded by default with a `+`.

???+ tip
    Use Admonition and Detail blocks for all sorts of information.

#### Types

??? example "Types of Admonition Blocks"
        !!! note
            Blocks are cool.
        
        !!! seealso
            Admonition types are also specified in the Material Theme docs.
    
    !!! note
        Blocks are cool.
        
    !!! seealso
        Admonition types are also specified in the Material Theme docs.
        
    ---
    
        !!! abstract
            This is a page detailing this site's Markdown syntax.
        
        !!! summary
            You can use admonition blocks to highlight specific info.
            
        !!! tldr
            Use three exclamation points followed by an ID.
            
    !!! abstract
        This is a page detailing this site's Markdown syntax.
    
    !!! summary
        You can use admonition blocks to highlight specific info.
        
    !!! tldr
        Use three exclamation points followed by an ID.
    
    ---
    
        !!! info
            This is an information block.
            
        !!! todo
            Write more docs!
    
    !!! info
        This is an information block.
        
    !!! todo
        Write more docs!
        
    ---
    
        !!! tip
            Insert a horizontal line with `---`.
            
        !!! hint
            Use an IDE so tabs aren't annoying.
        
        !!! important
            Always brush your teeth.
        
    !!! tip
        Insert a horizontal line with `---`.
        
    !!! hint
        Use an IDE so tabs aren't annoying.
    
    !!! important
        Always brush your teeth.
    
    ---
    
        !!! success
            You made an admonition block!
        
        !!! check
            Don't forget to turn the stove off before leaving home.
        
        !!! done
            You did it!
        
    !!! success
        You made an admonition block!
    
    !!! check
        Don't forget to turn the stove off before leaving home.
    
    !!! done
        You did it!
        
    ---
    
        !!! question
            What is the meaning of life?
        
        !!! help
            Help me, Obi-Wan Kenobi. You're my only hope.
        
        !!! faq
            FAQ stands for Frequently Asked Questions.
        
    !!! question
        What is the meaning of life?
    
    !!! help
        Help me, Obi-Wan Kenobi. You're my only hope.
    
    !!! faq
        FAQ stands for Frequently Asked Questions.
        
    ---
    
        !!! warning
            This is your last warning.
        
        !!! caution
            Here be dragons.
        
        !!! attention
            Please be advised.
    
    !!! warning
        This is your last warning.
    
    !!! caution
        Here be dragons.
    
    !!! attention
        Please be advised.
    
    ---
    
        !!! failure
            404 not found.
        
        !!! fail
            Oops!
        
        !!! missing
            Have you seen this block?
    
    !!! failure
        404 not found.
    
    !!! fail
        Oops!
    
    !!! missing
        Have you seen this block?
        
    ---
    
        !!! danger
            Mind the gap.
        
        !!! error
            Check your semicolons.
    
    !!! danger
        Mind the gap.
    
    !!! error
        Check your semicolons.
    
    ---
    
        !!! bug
            The ants go marching two-by-two, hurrah, hurrah.
        
    !!! bug
        The ants go marching two-by-two, hurrah, hurrah.
        
    ---
    
        !!! example
            This is an example of an example.
        
    
    !!! example
        This is an example of an example.

    ---
    
        !!! quote
            Any sufficiently advanced technology is indistinguishable from magic.
            
        !!! cite
            Clements, Jessica, Elizabeth Angeli, Karen Schiller, S. C. Gooch,
            Laurie Pinkert, Allen Brizee, and Vanessa Iacocca. 2017. “General Format.” 
            The Purdue OWL. Last edited October 12, 2017. 
            https://owl.english.purdue.edu/owl/resource/717/02.
        
    !!! quote
        Any sufficiently advanced technology is indistinguishable from magic.
        
    !!! cite
        Clements, Jessica, Elizabeth Angeli, Karen Schiller, S. C. Gooch,
        Laurie Pinkert, Allen Brizee, and Vanessa Iacocca. 2017. 
        “General Format.” The Purdue OWL. Last edited October 12, 2017. 
        https://owl.english.purdue.edu/owl/resource/717/02.

### Blockquotes
```markdown
> This is a blockquote.

> Blockquotes can have multiple paragraphs, 
and are not broken by newlines.

> > You can also nest them.
```

> This is a blockquote.

> Blockquotes can have multiple paragraphs, 
and are not broken by newlines.

> > You can also nest them.

### Math

    Put a TeX equation in its own block:
    $$
    \frac{n!}{k!(n-k)!} = \binom{n}{k}
    $$
    
Put a TeX equation in its own block:
$$
\frac{n!}{k!(n-k)!} = \binom{n}{k}
$$

### Lists

#### Unordered
    * A
    * simple
    * bulleted
    * list
    ---
    - You can also use `-` characters
    + In fact, lists can be `*`, `-`, or `+` characters
    * Even in the same list!

* A
* simple
* bulleted
* list
---
- You can also use `-` characters
+ In fact, lists can be `*`, `-`, or `+` characters
* Even in the same list!

#### Ordered

    1. You can make a numbered list.
    2. Count up.
    3. Up.
    4. And away!
    ---
    1. Another way is just using `1.` for everything.
    1. This is sometimes easier.

1. You can make a numbered list.
2. Count up.
3. Up.
4. And away!
---
1. Another way is just using `1.` for everything.
1. This is sometimes easier.

#### Indentation

    - Indents organize lists
        - Use indents by adding at least two spaces to the start of a line.
            - We need to go deeper.
    - And back out.
    ---
    1. Indented ordered lists:
        1. Will use alternate numbering for different indents.
            1. We're roman now!
        1. Otherwise, they follow the same procedure as ordered lists.
        You can put further list-item content on the same indent level.
        ```python
        print "Here's some code."
        ```
    1. Here's item 2.

- Indents organize lists
    - Use indents by adding at least two spaces to the start of a line.
        - We need to go deeper.
- And back out.
---
1. Indented ordered lists:
    1. Will use alternate numbering for different indents.
        1. We're roman now!
    1. Otherwise, they follow the same procedure as ordered lists.
    You can put further list-item content on the same indent level.
    ```python
    print "Here's some code."
    ```
1. Here's item 2.

#### Task Lists

    Shopping List:
    
    * [x] Bread
    * [x] Eggs
    * [ ] Milk
    * [ ] Ice cream
        * [x] Chocolate
        * [ ] Vanilla
    * [x] Chicken
    * [ ] Power cubes

Shopping List:

* [x] Bread
* [x] Eggs
* [ ] Milk
* [ ] Ice cream
    * [x] Chocolate
    * [ ] Vanilla
* [x] Chicken
* [ ] Power cubes

### Tables

#### Simple
    
    Widgets | Cost
    ---|---
    1 | $2
    50 | $75
    5000 | $5000


Widgets | Cost
---|---
1 | $2
50 | $75
5000 | $5000

#### Advanced

    | A left-aligned header.                             | A center-aligned header.         |       A right-aligned header. |
    |:---------------------------------------------------|:--------------------------------:|------------------------------:|
    | A long, *somewhat* complicated table element.      |       A centered element.        |                  `some code`. |
    | Another row in the table.                          | With the same number of columns. | [A link](https://google.com). |
    | The following cells are empty, as is the next row: |                                  |                               |
    |                                                    |                                  |                               |
    | And we're back.                                    |                                  |                         Whew. |

    

| A left-aligned header.                             | A center-aligned header.         |       A right-aligned header. |
|:---------------------------------------------------|:--------------------------------:|------------------------------:|
| A long, *somewhat* complicated table element.      |       A centered element.        |                  `some code`. |
| Another row in the table.                          | With the same number of columns. | [A link](https://google.com). |
| The following cells are empty, as is the next row: |                                  |                               |
|                                                    |                                  |                               |
| And we're back.                                    |                                  |                         Whew. |

Note that tables can have their pipes and contents either aligned or unaligned; whitespace and extra dashes are ignored.

### Images

    ![Some Title Text](../images/FIRSTlogo.svg)

![Some Title Text](../images/FIRSTlogo.svg)
