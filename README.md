# **My_Full_Stack_Web_Dev_Journey**

## **Section 5: Introduction to CSS**

### 1. Why do we need CSS ? 

        CSS - Cascading Style Sheets

-  "Cascading" -> cascades like a waterfall. 1. Start from the most general -> 2. All the way down to the most specific styling requirements. 

- "Style Sheets": A type of langauge similar to how we had the HTML. 
     - others: Saas, Less, etc..

=> basically adding style to our website. 

### 2. How do we add CSS ? 

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
    - 'html' that before the circular bracket are the selector, we put html in there to style the whole page
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

    > ## **How do we add CSS summary:** 
    > - ### Inline (for element only): `<html style =   "background:blue"> </html>`
    > - ### Internal (Single Webpage only): `<style> html {... value of attribute} </style>` in `<head>...</head>` tag
    > - ### External (Website, Multipage): style.css file
        






