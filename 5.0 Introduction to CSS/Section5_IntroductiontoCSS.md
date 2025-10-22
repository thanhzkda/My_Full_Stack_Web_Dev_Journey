# **Section 5: Introduction to CSS**

## 1. Why do we need CSS ? 

        CSS - Cascading Style Sheets

-  "Cascading" -> cascades like a waterfall. 1. Start from the most general -> 2. All the way down to the most specific styling requirements. 

- "Style Sheets": A type of langauge similar to how we had the HTML. 
     - others: Saas, Less, etc..

=> basically adding style to our website. 

## 2. How do we add CSS ? 

- Inline `<tag style="css" />`
    - Example: `<html style = "background:blue"> </html>`
        
        -> so the `style = "background:blue"` is the inline css
        
        `style` : name of the attribute.

        `background:blue`: value of the attribute, we add our css code in this.

        `background` is propety that you want to change; and `blue` is the value of that property that you want to set it to. 
    - Should be used if just need to style one specific object, not the whole page.
- Internal `<style>css</style>` 
    - Example: 
        ```
        <html>
            <head>
                <style>
                        html {
                            background:red; 
                        }
                </style>
            </head>
        </html>
        ```
    - 'html' that before the circular bracket are the css selector, we put html in there to style the whole page
    - But if you have a multipage and want to use same style, you should use "external" instead.
- External `<link href = "style.css/>`
    - In a completely different file, normally are "style.css"
    - How do we link it to our html ? 
        - Inside the head section of our html, we would add a 'link' element, which are self-closing.

        - Example: 
            ```
            <html>
                <head>
                    <link
                        rel = "stylesheet" 

                        <!-- rel mean relationship (basically asking what role are we adding to) -->

                        href = "./styles.css" 
                        
                        <!-- href = location (where it is located) -->
                    />
                </head>
            </html>
            ```

    >  **How do we add CSS summary:** 
    > -  Inline (for element only): `<html style =   "background:blue"> </html>`
    > -  Internal (Single Webpage only): `<style> html {... value of attribute} </style>` in `<head>...</head>` tag
    > -  External (Website, Multipage): style.css file
        

## 3. CSS Selectors: 
- As we known in internal `html {   background:red;  }`, `html` here is the CSS selector, but what it is actually ? 

- Its the part that selects the HTML in order to apply whichever rules go in between those curly bracket

>    Example: `html` here is the selector, so all the rules will apply to all `html` page, but if the selector now is `h1` or whatever, then all the rules inside the curly bracket will apply to all `h1` page.

- **Class Selector:** 
    ---
    
    - Syntax: 
        
        `.` then name of the class, then circular bracket with css code inside. (Note: No space between `.` and class name)
        ```
            .red-heading {  //red-heading is name of the class.
            color: red  //Change the color to red
            }
        ```
    - What is a class: Something that we can add as an attribute to any HTML element.
    - Example: 
        ```
        index.html
            <h2 class="red-text"> Heading 2</h2>
            <h3>Heading 3</h3>
            <p class="red-text">Paragraph</p>

        style.css
            .red-text{
                color:red;
            }
        
        Output: 
            "Heading 2", and "Paragraph" will both turn red
        ```
        => Allows you to group different parts of your HTML file into having the same styling

        => Useful on multi-page websites with lots of different elements.

- **Id Selector:**
    ---
    - Syntax:
        ```
        #main{
            color:red
        }
        ```
        => Has it own special symbol, pound sign (#), no space between # and Id name. 
    - Example: 
        ```
        index.html
            <h2 id="main">Red</h2>
            <h2>Green</h2>
            <h3>Blue</h3>

        style.css
            #main{
                color:red;
            }

        Ouput: "Red" will turn red.

    - What is it ? Same function as Class Selector.
    - What is the difference between id and class ?
        - Class Selector can be applied to many elements
        
        - Id: 
            - Should apply to only one element in single HTML file
            - Should only be one ID of the particular name
            - Should be unique and difference.
        
        > <em>"The Id should be applied to only one element in one single html file, and in a single HTML file (index.html), there should only be one ID of this particular name(main). It should be completely unique and difference."</em>

- **Attribute Selector**
    ---
    - Syntax: 
        ```
        p[draggable]{
            color:red
        }
        ```
        `p` html element,
        `[...]` inside the square bracket is attribute

        **<em>Purpose: </em>** Select all p elements with the attribute draggable and then apply the CSS style ('color:red) into it.

    - Example: 
        ```
        index.html
            <p draggable="true">Drag me</p>
            <p>Don't drag me</p>
            <p>Don't drag me</p>

        style.css
            p[draggable]{
            color:red
            }

        Output: 
            "Drag me" will turn red.
        ```

        but if: 
        ```
        index.html
            <p draggable="true">Drag me</p>
            <p draggable="false">Don't drag me</p>
            <p draggable="false">Don't drag me</p>

        style.css
            p[draggable="false"]{
            color:red
            }

        Output: 
            All "Don't drag me" will turn red.

- **Universal Selector**
    ---
    - Syntax: 
        ```
        *{
            color:red
        }
        ```
        => Meaning: Select all.
    > Doesn't matter what class you got, what ID, what attribute set, which different elements, if you use this it will select all and apply the style to everything where the stylesheet is active.
    


    

# HOMEWORK: 5.2 CSS