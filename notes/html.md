# NOTES

## HTML notes

The line below is used for mobile responsivity

        <meta name="viewport" content="width=device-width, initial scale=1.0"/>

Form - post - action - submit

        <form method="post" action="submit-to-URL">
        <section></section>
        </form>

### Accessibility tools (Keyboard shortcuts and ARIA attributes)  

**ROLE** attribute can be used to indicate the purpose behind the element on the page to assistive technologies.  
The **ROLE** attribute is a part of the *Web Accessibility Initiative* (WAI), and accepts preset values.  
Every **ROLE** needs a label. One method of adding a label is by adding a heading element inside it and reference is as **ARIA-LABELLEDBY** attribute.  
**label - for** - It is important to link each input to the corresponding label element. This provides assistive technology users with a visual reference to the input.

### Keyboard shortcuts

**ALT+Z** - toggle word wrap in command line interface    
**ALT+Left Click** - create multiple cursors  
**CTRL+SHIFT+L** - Select and replace all reocurrence  
**CMD+/** - comment the selected text or line  


## CSS notes

Asterisk means all html elements.  
Styling priority is #id>.class>child_element>parent_element.  
Style that takes over when the browser meet the minimum width requirement.  

        @media (min-width; 540px) {

        }
        
Another type of selector 

        *input[type="submit"]* {
                
        }

### Accessibilities to keep in mind

Typeface plays and important role in accessibility of a page. Some fonts are easier to read that others, and this is especially true to low-resolution screens.

## GIT hub notes

Try to make a daily commit to paint the activity more green.

## CSS tips

1. Choose good color scheme.  
2. Master **flexbox**. Rows and columns and subsequent rows and columns.  
3. **Responsivity** - start to design in mobile first for overall better responsivity.  
4. Memorize breakpoints. Breakpoints are the widths or dimensions of the page of which the styling  changes to retain responsivity.  
    - small - 640px     >
    - medium - 768px    > use in media query *@media (min-width: value)*
    - large - 1024px    >
5. jankcss.com

