# Frontend Mentor - Loopstudios landing page solution

This is a solution to the [Loopstudios landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/loopstudios-landing-page-N88J5Onjw). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![Screenshot of the Loopstudios landing page](./screenshot.gif)

### Links

- Solution URL: [Github](https://github.com/snigdha-sukun/loopstudios-landing-page)
- Live Site URL: [Vercel](https://loopstudios-landing-page-bice.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- SCSS
- Flexbox
- CSS Grid
- JS

### What I learned

I learned how to use SCSS. I was able to create `@mixin` with condition using `@if` and variables. I also learned how to use `@content` to define `@mixin` for mobile view.

```scss
@mixin mobile {
    @media (max-width: 768px) {
        @content;
    }
}

@mixin responsive-grid($columns, $rows: null) {
    @include display-grid($columns);

    @if $rows {
        grid-template-rows: repeat($rows, 1fr);
    }

    @include mobile {
        @include display-flex(space-between, column);
    }
}
```

I also leanred how to show the text over an image without losing the opacity of the text on hover:

```scss
.creation__card {
    position: relative;
    text-align: center;
    color: v.$white;
    cursor: pointer;
}

.creation__card img {
    transition: opacity 0.3s ease-in-out;
}

.creation__card:hover img,
.creation__card:focus img {
    opacity: 0.3;
}

.creation__card:hover .card__text,
.creation__card:focus .card__text {
    color: v.$black;
}

.card__text {
    position: absolute;
    bottom: 1%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

### Continued development

I want to continue learning & practice different CSS methodologies and SCSS.

### Useful resources

- [Position Text Over an Image](https://www.w3schools.com/howto/howto_css_image_text.asp) - This helped me position Text Over an Image in the creation cards.
- [Sass Basics](https://sass-lang.com/guide/) - This was a good starting point to learn the basics.
- [Learn Sass In 20 Minutes](https://www.youtube.com/watch?v=Zz6eOVaaelI) - This helped me in learning about the VSCode extention to use for Sass file processing.

## Author

- Frontend Mentor - [@snigdha-sukun](https://www.frontendmentor.io/profile/snigdha-sukun)
