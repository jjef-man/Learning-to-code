# NOTES

## HTML notes

### Websites for html resources:  

**fonts.google.com** - fonts  
**fontawesome.com** - icons  
**cdnjs.com/libraries/font-awesome** - where to get the resource code to use the icons from fontawesome  

### Codes to note

First thing to code in .html

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Document</title>
            <link rel="stylesheet" href="styles.css" />
        </head>
        <body>
    
        </body>
        </html>

Form - post - action - submit

        <form method="post" action="submit-to-URL">
        <section></section>
        </form>

Navigate through the page  

        <a href="#footer"></a>
        <footer id="footer"></footer>

### Keyboard shortcuts

**ALT+Z** - toggle word wrap in command line interface    
**ALT+Left Click** - create multiple cursors  
**CTRL+SHIFT+L** - Select and replace all reocurrence  
**CMD+/** - comment the selected text or line  
**SHIFT+ALT+F** - automatically indent the lines (WIN)  
**SHIFT+OPTION+F** - autumatically indent the lines (MAC)  

### Accessibility tools (Keyboard shortcuts and ARIA attributes)  

- **ROLE** attribute can be used to indicate the purpose behind the element on the page to assistive technologies.  
- The **ROLE** attribute is a part of the *Web Accessibility Initiative* (WAI), and accepts preset values.  
- Every **ROLE** needs a label. One method of adding a label is by adding a heading element inside it and reference is as **ARIA-LABELLEDBY** attribute.  
- **Label - for** - It is important to link each input to the corresponding label element. This provides assistive technology users with a visual reference to the input.  
- The **accesskey** attribute accepts a space-separated list of access keys.  
For example:  

        <button type="submit" accesskey="s">Submit</button>



## CSS notes

Asterisk means all html elements.  
Styling priority is #id>.class>child_element>parent_element.  
Style that takes over when the browser meet the minimum width requirement.  

        @media (min-width; 540px) {

        }

        @media (feature: value) {
          selector {
            styles
          }
        }

Used to make the bullet stick to the text of the list

        ul  {
          padding-left: 0;
        }
        ul li {
           list-style-position: inside;
        }
        
Another type of selector 

        *input[type="submit"]* {
                
        }

Display grid

        body {
                display: grid;
                grid-template-columns: repeat(1, minmax(0,1fr));
        }
        
             /* grid-template-columns: repeat(4, minmax(0,1fr));
                grid-template-columns: minmax(2rem, 1fr) minmax(min-content, 94rem) minmax(2rem, 1fr);
                grid-template-columns: repeat(2, 1fr);
                grid-template-columns: 1fr 2fr;
                column-width: 25rem;
             */
                
        .element {
                grid-column: span 3/ span 3;
                grid-column: 2 / 3;
                grid-auto-flow: column;
                grid-auto-columns: 1fr;
        }

Position item in center using grid

        .element {
                display: grid;
                place-items: center;
        }

Z-index

        .element {
                position: relative;
                z-index: 1;
        }

Change the color of highlight when a text is selected

        p::selection,
        h1::selection,
        h2::selection {
                background-color: black;
                color: white;
        }

Smooth scrolling

        html {
                scroll-behavior: smooth;
        }

Before/after psuedo elements

        nav::before {
            content: '';
            position: absolute;
            inset: 0;
            background-color: transparent;
            opacity: .1;
            box-shadow: 0 0 5px 2px black;
        }

CSS animation

        @keyframes [name] {
          0% {
    transform: rotate(0deg);
          }
          25% {
    background-color: yellow;
          }
          50% {
    background-color: purple;
          }
          100% {
    transform: rotate(-360deg);
          }
        }

        [selector] {
                animation-name: [name];
                animation-duration: 5s; or ms
                animation-timing-function: linear; or ease-in-out
                animation-iteration-count: infinite; or definite time value
        }

        [selector] {
                animation: [name] 5s linear infinite;
        }
        
### Accessibilities to keep in mind

Typeface plays and important role in accessibility of a page. Some fonts are easier to read that others, and this is especially true to low-resolution screens.  
CSS Codes to hide a text for screen readers

        .sr-only {
          position: absolute;
          width: 1px;
          height: 1px;
          padding: 0;
          margin: -1px;
          overflow: hidden;
          clip: rect(0, 0, 0, 0);
          white-space: nowrap;
          border: 0;
        }

## CSS tips

1. Choose good color scheme.  
2. Master **flexbox**. Rows and columns and subsequent rows and columns.  
3. **Responsivity** - start to design in mobile first for overall better responsivity.  
4. Memorize breakpoints. Breakpoints are the widths or dimensions of the page of which the styling  changes to retain responsivity.  
    - small - 640px     >
    - medium - 768px    > use in media query *@media (min-width: value)*
    - large - 1024px    >
5. jankcss.com

## Tailwind CSS notes

### Starting a Tailwind CSS porject

The steps can be found in the link below:  
https://tailwindcss.com/docs/guides/vite

## JavaScript notes

### Primitive

1. **Number** - numerical values, including integers, decimals, and exponents. *(e.g., 1, 3.14, 1e5)*.  
2. **String** - sequences of characters enclosed in quotes. *(e.g., "Jane's", 'Hello', "")*.  
3. **Boolean** - truth values, either true or false. *(e.g., true, false)*.  
4. **Null** - absence of a value. It's different from undefined. *(e.g., null)*.  
5. **Undefined** - absence of a value due to not being assigned yet or a reference pointing to nowhere. *(e.g., undefined)*.  
   
### Object

1. **Object *(or dictionary)*** - is a complex data type that allows you to store collections of key-value pairs.   *{ name: Jane, age: 25 }*.  
2. **Array *(or list)*** - is a special type of object used to store ordered collections of values.   *[1, 2, 3, 4]*.  
3. **Function** - is a subtype of object that can be invoked/called.   *function add(x, y) { return x + y; }*.

### Arithmetic Operators

Addition (+): let sum = 5 + 6  
Subtraction (-): let difference = 11 - 2  
Multiplication (*): let product = 8 * 6  
Division (/): let quotient = 10 / 5  
Modulus (%): let remainder = 8 % 3; // 2 (remainder)  

### Assignment Operators

Assignment (=): let x = 1;  

### Comparison Operators

Equal (==): let isEqual = 5 == '5'; // true (loose equality, type coercion)  
Strict Equal (===): let isStrictEqual = 5 === '5'; // false (strict equality, no type coercion)  
Not Equal (!=) and Not Strict Not Equal (!==): let notEqual = 10 != '10'; // false let strictNotEqual = 10 !== '10'; // true  

### Logical Operators

Logical AND (&&):  
Logical OR (||):  
Logical NOT (!):  

### Other Operators

typeof Operator: let type = typeof variable; // Returns the type of the variable  
