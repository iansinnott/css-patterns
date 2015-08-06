# CSS Idioms

Simple solutions to the most common problems we face when authoring CSS.

## Why?

I write a lot of CSS (well, [Stylus][] actually) and I often find myself reaching for the same CSS patterns over and over again. So I finally decided I should really write these down somewhere, for my own sake at least and hopefully for the benefit of others too. Let's jump in.


## Terminology

- **Fixed Size:** Any value defined by you that . Example: `width: 200px;`, `padding: 2%;`
    
    Examples of non-fixed, or partially-fixed size would be `width: auto;`, `margin: 0 auto;`

- **Variable Size:** When an elements size is dependent on the content you put inside it. This is the default for most block elements

## General Rules

### Use a preprocessor

You'll be doing yourself a huge favor. Even if you pre-process [CSS Next][] down to regular CSS this is a big win. Once you write nested styles and variables you will never go back to plain CSS. 

Here are some options:

* [Stylus][]
* [Sass][]
* [Less][]
* [CSS Next][]

My favorite is [Stylus][], but use what you feel most comfortable with. The snippets you will find here are all written in Stylus, but I've included a compiled plain CSS file for anyone who's uncomfortable with Stylus syntax. 

[Stylus]: https://learnboost.github.io/stylus/
[CSS Next]: https://github.com/cssnext/cssnext
[Sass]: http://sass-lang.com/
[Less]: http://lesscss.org/

## Layout

CSS layout, if anything, is often the most vexing part of creating CSS. For that reason most of the idioms to follow revolve around achieving some layout.

### Vertical Center

- **Fixed Size Vertical Center:**
  
    If you're targetting only browsers that aren't terrible you can use the nifty `transform translateY(-50%)` in conjunction with absolute positioning:

    ```stylus

    // Containing element needs position relative of course
    .vertical-center-parent
      position relative

    // 
    // By translating the element up (using a negative percentate)
    .vertical-center
      position absolute
      top 50%
      transform translateY(-50%)
    ```

    However, if you or your requirements insist on supporting terrible browsers you'll have to resort to the `display table` method: 
- **Variable Size Vertical Center:**

### Horizontal Center

- **Fixed Size Vertical Center:**
- **Variable Size Vertical Center:**

### Absolute Center
