# Blogger Site
## by: Chris Jones
### 12-01-2020

I am going to build a blogging website for my portfolio.
If I make a website everyday I will have alot
of stuff to work with and show potential employers/clients and will
give me a chance to brush up on my HTML and CSS / flexbox.

#### THE HTML

```
<!DOCTYPE html>
<html lang="en">	
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blogger Template</title>
    <!-- Custom Style -->
    <link rel="stylesheet" href="./css/main.css">
</head>
<body>
    <!---------------------------- Navigation --------------------------->
    <nav class="nav">
        <div class="nav-menu flex-row">
            <div class="nav-brand">
                <a href="#" class="text-grey">Blogger</a>
            </div>
            <div>
                <ul class="nav-items">
                    <li class="nav-link">
                        <a href="#">Home</a>
                    </li>
                    <li class="nav-link">
                        <a href="#">Category</a>
                    </li>
                    <li class="nav-link">
                        <a href="#">Archive</a>
                    </li>
                    <li class="nav-link">
                        <a href="#">Pages</a>
                    </li>
                    <li class="nav-link">
                        <a href="#">Contact Us</a>
                    </li>
                </ul>
            </div>
            <div class="social text-gray">
                <a href="#">F</a>
                <a href="#">IG</a>
                <a href="#">T</a>
                <a href="#">Y</a>
            </div>
        </div>
    </nav>
    <!------------x--------------- Navigation ---------------x----------->

 <!-- custom JS -->
<script src="./js/main.js"></script>
</body>
</html>
```

<br> 
THE CSS: 
<br>

```
html,
body {
  margin: 0%;
  box-sizing: border-box;
  overflow-x: hidden;

}

/*---------- Global Classes ----------*/

a {
  text-decoration: none;
}

.flex-row {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

ul {
  list-style-type: none;
}
/*---------- Global Classes ----------*/

/*--------- navbar -------*/

.nav {
  background: white;
  padding: 0 2rem;
  height: 0rem;
  min-height: 40vh;
}

.nav .nav-menu {
  justify-content: space-between;
}

.nav .nav-items {
  display: flex;
  margin: 0;
}

.nav .nav-items .nav-link {
  padding: 1.6rem 1rem;
  font-size: 1.1rem;
  position: relative;
}

.nav .nav-brand a {
  font-size: 1.6rem;
  padding: 1rem 0;
  text-decoration: none;
  display: block;
}

.nav .social {
  padding: 1.4rem 0;
}

/*----x---- navbar ---x---*/

```

<br>
### Adding the Social Icons.

In this section we are going to add the social icons to the
navigation using fontawesome.

download fontawesome from the [website](http://www.fontawesome.com)
extract the files, and copy the `all.css` file and the `web fonts` folder.

#### How to implement on the site.

`<i class = "fas fa-camera"></i>`<br><br>
`<i class = "fas fa-camera"></i>`<br><br>
`<span class ="fas fa-camera></span>`<br><br>

Be sure to link the `all.css` file in your index file, and
use `<i class="fab fa-instagram">` to put what ever icon you want to use on your page.

# Fonts

How to add fonts from google to your site

[fonts.google.com](http://fonts.google.com)

The following fonts are used in this project:

```

Abel

Livvic

Lexend Deca

Josefin Sans

Anton

```

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

_NOTE: If you are using VScode just type `--name of variable` and VScode will automatically put the ``var` keyword_

# Colors

Use color variables.

```

a {
	text-decoration: none;
	color: #3f4959;
}

```

within the root properties like with the fonts place the variable:

` --text-grey: #3f4954;`

now when I want to use that color on something all I have to do is put `--text-grey` and vs code will make it `var(--text-grey);`

[colors.co](http://colors.co)

To get cool color themes and their HEX values.

# Gradient Color

[webgradients.com](http:/webgradients.com)

This site has a log of really cool pre made gradients and you can just copy the css and make a variable for it too with the other colors:

`--sky: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);`

---

<!-- added nav hover effect on links and social -->

# Responsive Navigation

To make the nav bar responsive we need to use media queries.

# Media Queries

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

This will position the hamburger menu over to the right side of the nav menu using the media query 750px.

# Show / hide Hamburger Menu

on the `.nav .toggle-collapse` selector add `display: none;

Then in the `750px` media query put:

```

.nav .toggle-collapse {
    display: initial;
  }

```

`This will only display the hamburger menu when the width of the web page is at`750px` or less.

# Jquery

[jquery.com](htt://www.jquery.com)

Go to downloads and copy the compressed jquery file
make a new file called `jquery.3.4.1.min.js` and paste the code, be sure to save it.

[ need to come back to this.. ]

---
#### 12/07/2020
# The Header

The header is the content at the top of the page, usually a large colorful background, a title and usually a call to action button of some kind.

This is just some basic HTML and CSS.

---
# Owl Carousel 
[Owl Carousel gethub](https://owlcarousel2.github.io/OwlCarousel2/)

download the files in a zip file then copy the main owl carousel js file into your projects js folder, then copy the css file and the them file into your projects css folder.

Make sure to link all three of the files in the HTML file. 2 CSS and 1 JS.

THE HTML:

```

 <section>
            <div class="blog">
                <div class="container">
                    <div class="owl-carousel owl-theme blog-post">
                        <div class="blog-content">
                            <img src="./assets/Blog-post/post-1.jpg" alt="post-1">
                            <div class="blog-title">
                                <h3>London Fashion Week's Continued the evolution</h3>
                                <button class="btn btn-blog">Fashion</button>
                                <span>2 minutes</span>
                            </div>
                        </div>
                        <div class="blog-content">
                            <img src="./assets/Blog-post/post-3.jpg" alt="post-3">
                            <div class="blog-title">
                                <h3>London Fashion Week's Continued the evolution</h3>
                                <button class="btn btn-blog">Fashion</button>
                                <span>2 minutes</span>
                            </div>
                        </div>
                        <div class="blog-content">
                            <img src="./assets/Blog-post/post-2.jpg" alt="post-2">
                            <div class="blog-title">
                                <h3>London Fashion Week's Continued the evolution</h3>
                                <button class="btn btn-blog">Fashion</button>
                                <span>2 minutes</span>
                            </div>
                        </div>
                        <div class="blog-content">
                            <img src="./assets/Blog-post/post-5.png" alt="post-5">
                            <div class="blog-title">
                                <h3>London Fashion Week's Continued the evolution</h3>
                                <button class="btn btn-blog">Fashion</button>
                                <span>2 minutes</span>
                            </div>
                        </div>
                    </div>

                    <div class="owl-navigation">
                        <span class="owl-nav-prev"><i class="fas fa-long-arrow-alt-left"></i></span> 
                        <span class="owl-nav-next"><i class="fas fa-long-arrow-alt-right"></i></span>

                    </div>
                </div>
            </div>
        </section>

```

THE CSS:

```

main .blog {
  background: url('../assets/Abract01.png');
  background-repeat: no-repeat;
  background-position: right;
  background-size: 65%;
  padding-top: 6rem;
  height: 100vh;
  width: 100%;

}

main .blog .blog-post {
  padding-top: 6rem;

}

main .blog-post .blog-content {
  display: flex;
  flex-directioN: column;
  text-align: center;
  width: 80%;
  margin: 3rem 2rem;
  box-shadow: 0 15px 20px rgba(0,0,0,0.2);
}

main .blog-content .blog-title {
  padding: 2rem 0;

}

main .blog-content .btn-blog {
  padding: .7rem 2rem;
  background: var(--sky);
  margin: .5rem;
}

main .blog-content span {
  display: block;

}

section .container .owl-nav {
  position: absolute;
  top: 0%;
  margin: 0 auto;
  width: 100%;
}

.owl-nav .owl-prev .owl-nav-prev, 
.owl-nav .owl-next .owl-nav-next {
  color: var(--midnight);
  background: transparent;
  font-size: 2rem;
  
}

.owl-theme .owl-nav [class*='owl-']:hover {
  background: transparent;
  color: var(--text-grey);
  border: none;
}

.owl-theme .owl-nav [class*='owl-']{
  outline: none;
}

```

JS:

```

 $('.owl-carousel').owlCarousel({
        loop: true,
        autoplay: true,
        autoplayTimeout: 3000,
        dots: false,
        nav: true,
        navText: [$('.owl-navigation .owl-nav-prev'),$('.owl-navigation .owl-nav-next')]
    });

```



Don't forget to link the JS.

```

 <!-- Carousel-JS -->
    <script src="./js/owl.carousel.min.js"></script>

```



# Site Content

Here I am going to create two columns using CSS Grid.

### How to use CSS Grid:
In the HTML make two divs one called posts and one called sidebar which is an HTML5 aside. Next, in the CSS I put `display: grid` and added the two columns `grid-template-column: 70% 30%` See code below.

HTML:

```

<section class="container">
	<div class="site-content">
    	<div class="posts">
        	<h1>Blog Posts</h1>
        </div><!-- end blog posts -->
        <aside class="sidebar">
        	<h1>Sidebar</h1>
        </aside>
    </div>
</section>

```

CSS:

```

main .site-content {
	display: grid;
	grid-template-column: 70% 30%;
}

```

`&nbsp;` = none breaking space.

I have finished the first blog post. Now to just copy and paste and change the content to add more blog posts on the site-content section.

Added the pagination.

# Side Bar

### Popular Posts
Here I basically copied the blog posts and added them to the side bar. I changed the pictures.

### Newsletter
Added a text form with a button under it.

### Popular Tags
Added a popular tags section to the bottom of the side bar.
