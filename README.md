<!-- continuing the font awesome from file on desktop -->

Be sure to link the `all.css` file in your index file, and 
use `<i class="fab fa-instagram">` to put what ever icon you want to use on your page.

## FONTS


How to add fonts from google to your site

[fonts.google.com](http://fonts.google.com)

The following fonts are used in this project:

---
`Abel`

`Livvic`

`Lexend Deca`

`Josefin Sans`

`Anton`

---


You can `<link>` the fonts, or download the fonts and use use `@import`.


In this instance I downloaded the fonts, and will import them into the HTML file.

once the fonts are donwloaded, extract them into a `fonts` folder in the root directory of your project.

This folder should now be visible in VScode.
In the CSS folder create a file called `fonts.css`

```

/* font-family: Abel */

@font-face {
    font-family: Abel;
    src: url('../fonts/Abel/Abel-Regular.ttf')
}

```  
This is what it should look like when you declare a font. Do this to each of the fonts for the project.
 
Now, in the CSS file:

`@import url(./css/fonts.css')`
 
I should be able to use these fonts now in my HTML document.
 
In the main CSS file this how to change the font for the Title H1
 
`font-family: Abel,cursive;`

# Font Variables 
 
 To make a font variable in your main CSS file go up to the top where the HTML styles are:  

```

:root {
  /* theme font-family */
  --Abel: 'Abel',cursive;
}

```

and then in the CSS where you want the font to be:

`font-family: var(--Abel);` 

use the key word `var` for variable and then put in the name you gave up above where the HTML styles are.

*NOTE: If you are using VScode just type `--name of variable` and VScode will automatically put the ``var` keyword* 


# COLORS

Use color variables.

```
a {
	text-decoration: none;
	color: #3f4959;
}
```

within the root properties like with the fonts place the variable:

`  --text-grey: #3f4954;`

now when I want to use that color on something all I have to do is put `--text-grey` and vs code will make it `var(--text-grey);`

[colors.co](http://colors.co)

To get cool color themes and their HEX values.

# gradient color

[webgradients.com](http:/webgradients.com)
  
This site has a log of really cool pre made gradients and you can just copy the css and make a variable for it too with the other colors:

`--sky: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);`

---

<!-- added nav hover effect on links and social -->

# RESPONSIVE NAV

To make the nav bar responsive we need to use media queries.

# Media Queries.

Media queries are like set points where you want the style of the page to change like have a media query for mobile, one for tablet, and one for Desktop for instance.

use this block of code in the CSS:

```
@media only screen and (max-width: 750px) {
 /* CSS styles go here */* 
}
```

Now I can put whatever CSS styling you want the page to have for the specified 750px width. this is about the size of a small tablet.

# The Hamburger Menu

HTML:  

```
<div class="toggle-collapse">
                <div class="toggle-icons">
                    <i class="fas fa-bars"></i>
                </div>
            </div>
            
```
            

This will create the hamburger menu, I have it inside of the `.nav .toggle-collapse .toggle-icons` div.

CSS:

```

.nav .toggle-collapse {
  position: absolute;
  top: 0%;
  width: 90%;
  cursor: pointer;

}

.nav .toggle-collapse .toggle-icons {
  display: flex;
  justify-content: flex-end;
  padding: 1.7rem 0;
}

```

This will position the hamburger menu over to the right side of the nav menu.





