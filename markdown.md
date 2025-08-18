## Basic Components of Markdown Documentation

Markdown documentation primarily uses plain text with special characters to indicate formatting. Here's a basic list of its components:

-----

### Headings

Headings are used to create titles and subtitles, similar to HTML heading tags. They are denoted by hash symbols (`#`) at the beginning of a line.

  * **Syntax:**
    ```markdown
    # Heading 1
    ## Heading 2
    ### Heading 3
    #### Heading 4
    ##### Heading 5
    ###### Heading 6
    ```

-----

### Paragraphs

Paragraphs are simply blocks of text. You create a new paragraph by leaving a blank line between lines of text.

  * **Syntax:**
    ```markdown
    This is the first paragraph.

    This is the second paragraph, separated by a blank line.
    ```

-----

### Emphasis

You can make text **bold** or *italic* using asterisks (`*`) or underscores (`_`).

  * **Syntax:**
    ```markdown
    *italic text* or _italic text_
    **bold text** or __bold text__
    ***bold and italic text*** or ___bold and italic text___
    ```

-----

### Lists

Markdown supports both ordered (numbered) and unordered (bulleted) lists.

  * **Ordered Lists:** Start each item with a number followed by a period.
      * **Syntax:**
        ```markdown
        1. First item
        2. Second item
        3. Third item
        ```
  * **Unordered Lists:** Use hyphens (`-`), asterisks (`*`), or plus signs (`+`).
      * **Syntax:**
        ```markdown
        - Item one
        - Item two
            * Sub-item A
            * Sub-item B
        ```

-----

### Links

Links allow you to embed hyperlinks to other web pages or sections within the same document.

  * **Syntax:**
    ```markdown
    [Link Text](URL)
    [Google](https://www.google.com)
    ```

-----

### Images

You can embed images using a similar syntax to links, but with an exclamation mark (`!`) at the beginning.

  * **Syntax:**
    ```markdown
    ![Alt text](Image URL "Optional title")
    ![Markdown Logo](https://markdown-here.com/img/icon256.png "Markdown Icon")
    ```

-----

### Code Blocks and Inline Code

Markdown is excellent for displaying code.

  * **Inline Code:** Use backticks (`` ` ``) for small snippets of code within a line.
      * **Syntax:**
        ```markdown
        To display inline code, use `print("Hello, World!")`.
        ```
  * **Code Blocks:** Use three backticks (`` ``` ``) before and after a block of code. You can also specify the language for syntax highlighting.
      * **Syntax:**
        ````markdown
        ```python
        def hello_world():
            print("Hello, Markdown!")
        ```
        ````

-----

### Blockquotes

Blockquotes are used for quoting text, similar to how quotes are presented in emails. They are denoted by a greater-than sign (`>`).

  * **Syntax:**
    ```markdown
    > This is a blockquote.
    > It can span multiple lines.
    ```

-----

### Horizontal Rules

Horizontal rules are used to create thematic breaks in your content. They are created using three or more hyphens (`-`), asterisks (`*`), or underscores (`_`).

  * **Syntax:**
    ```markdown
    ---
    ***
    ___
    ```