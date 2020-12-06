<!-- continuing the font awesome from file on desktop -->

Be sure to link the `all.css` file in your index file, and 
use `<i class="fab fa-instagram">` to put what ever icon you want to use on your page.

### Using Fonts


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