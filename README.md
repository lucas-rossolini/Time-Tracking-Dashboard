# Frontend Mentor - Time tracking dashboard solution

This is a solution to the [Time tracking dashboard challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/time-tracking-dashboard-UIQ7167Jw). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Switch between viewing Daily, Weekly, and Monthly stats

### Screenshot

![dashboard screenshot](./images/screenshot.png)

### Links

- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Javascript

### What I learned

This was my first real DOM maniulation exercise with javascript. I learned how to create a full element only using javascript and dynamic informations.

```js
function createNewCard(duration) {
  for (i = 0; i < myData.length; i++) {
    let oldSection = document.querySelector(`#${myData[i].idSection}`);
    oldSection.remove();
  }
  for (i = 0; i < myData.length; i++) {
    let newSection = document.createElement("section");

    const cards = document.querySelector("#cards");

    newSection.classList.add("card-section");
    newSection.setAttribute("id", myData[i].idSection);

    let el = `<div class="head">`;
    el += myData[i].svgSection;
    el += `</div>`;
    el += `<div class="contain">`;
    el += `<div class="contain-head">`;
    el += `<h5 class="contain-title">${myData[i].title}</h5>`;
    el += `<a class="contain-dots" href="">•••</a>`;
    el += `</div>`;
    el += `<div class="duration">`;
    el += `<p class="current-duration">${myData[i].timeframes[duration].current} hrs</p>`;
    el += `<p class="previous-duration">Last ${myData[i].timeframes[duration].timing} - ${myData[i].timeframes[duration].previous} hrs</p>`;
    el += `</div>`;
    el += `</div>`;

    newSection.innerHTML = el;

    cards.appendChild(newSection);
  }
}
```

### Continued development

For my next project I will focus on using React more than using scripts in an HTML document.


## Author

- Github - [Lucas Rossolini](https://github.com/lucas-rossolini)

