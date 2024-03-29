# The Best CSS Reset of 2024!

## Table of contents

- [Table of content](#table-of-content)
- [Box sizing](#box-sizing)
- [Margin and padding](#margin-and-padding)
- [List decoration](#list-decoration)
- [Scroll behavior](#scroll-behavior)
- [Link underline](#link-underline)
- [Image and videos](#image-and-video-settings)
- [Inputs](#inputs)
- [Prefers reduced motion](#prefers-reduced-motion)
- [The Body and HTML](#the-body-and-the-html-elements)
  
## Box sizing
```css
*, *::before, *::after{
    box-sizing: border-box; 
}
```
This sets the percived size of the element in the DOM to include its **border**.

## Margin and padding
```css
*{
    margin: 0; 
    padding: 0; 
}
```
Because some HTMl elements have default margins and paddings on them, this sets the default margin and padding behavior to **0**.

## List decoration
```css
ul[role='list'], ol[role='list']{
    list-style: none; 
}
```
For all **ordered** and **unordered lists**, turn off the **decoration** (the number and dots).

## Scroll behavior 
```css
html:focus-within{
    scroll-behavior: smooth; 
}
```
Set the **scroll behavior** of all scrollable elements to **smooth**.

## Link underline
```css
a:not([class]){
    text-decoration-skip-ink: auto; 
}
```
Make the **link underlines** and **normal underlines** skip the **"hooky"** letters and symbols (q, y, j, g). Makes them look more natural.

## Image and video settings
- ### Responsiveness
  ```css
  img, picture, svg, video, canvas{
    max-width: 100%;
    height: auto;
  }
  ```
  Images aren't **repsonsive by default**, and they become by setting this. **Magic**.
- ### Inline images
  ```css
  img, picture, svg, video, canvas{
    vertical-align: middle; 
  }
  ```
  This sets the **inline immages** to align with the text next to them.
- ### Font on images _? (stay with me)_
  ```css
  img, picture, svg, video, canvas{
    font-style: italic; 
  }
  ```
  In the case an images **doesn't load**, setting and alternative text that explains the image and that is **italic** tells the user.
- ### Backroung images
  ```css
  img, picture, svg, video, canvas{
    background-repeat: no-repeat; 
    background-size: cover;
  }
  ```
  If you want to set an image as a **background** but the _connection is slow_, a **worse quality image** will load first, while the real one loads.

## Inputs
```css
input, button, textarea, select{
  font: inherit; 
}
  ```
Make these elements **inherit fonts** from parent elements.

## Prefers reduced motion 
```css
@media (prefers-reduced-motion: reduce){
    html:focus-within {
        scroll-behavior: auto;
    }
    *, *::before, *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
        scroll-behavior: auto !important;
        transition: none;
    }
}
```
Simply put, this turns off **animations** for people who don't want to see them. (The only usecase for _**!important**_)

## The Body and The HTML elements
```css
body, html{
    height: 100%; 
    scroll-behavior: smooth; 
}
```
This makes the elements full screen while keeping the scrolling smooth.
