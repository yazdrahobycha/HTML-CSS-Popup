# HTML and CSS Pop-up for Kottans

This is a solution to the "HTML and CSS Pop-Up" task by [Kottans](https://github.com/kottans).

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
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements
- The popup must functionality be designed to have three distinct modes based on user interactions:
  - Initial Mode: The popups are not displayed.
  - Activation Mode: Upon clicking the popup button, the popup becomes either visible or hidden, depending on its current state.
  - Expansion Mode: By clicking the "More" button, 3 to 10 additional icons can be added to the popup, making the contents scrollable.


### Screenshot

<p align="center">
  <img src="img/Снимок экрана 2023-02-11 в 11.42.47.png" alt="Project Photo"/>
</p>

### Links

[Demo](https://yazdrahobycha.github.io/HTML-CSS-Popup/) | [Pull-Request](https://github.com/kottans/frontend-2019-p2p/pull/215)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- SVG Backgrounds

### What I learned

The project was a roller coaster of emotions, but mostly excitement! I thought manipulating checkboxes would be a walk in the park, but boy, was I in for a surprise. Trying to arrange them with the focus state was like playing a game of Jenga, one wrong move and everything comes tumbling down. But, with perseverance and a few burnt midnight oil, I finally got the hang of it:

<details>
<summary>CSS for Pop-Up, using checkboxes </summary>

```css
.popup__checkbox:checked ~ .popup {
    display: block;
}

.popup__list,
.more:checked ~ .popup__more {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    justify-content: center;
    gap: 0.5rem;
}

.more:checked ~ .more__btn,
.popup__more {
    display: none;
}

.popup__more {
    margin-top: 0.5rem;
}
```

</details>

And for the first time, I attempted to utilize the `<svg>` element for styling the background. The outcome was rather intriguing, adding some liveliness to the design:

<details>
<summary>CSS for SVG background </summary>

```css
.banner__foreground {
    border: 3px solid black;
    z-index: 2;
    position: relative;
}

.banner__background {
    width: 100%;
    height: 100%;
    background-image: url("data:image/svg+xml,<svg id='patternId' width='100%' height='100%' xmlns='http://www.w3.org/2000/svg'><defs><pattern id='a' patternUnits='userSpaceOnUse' width='40' height='40' patternTransform='scale(0.17) rotate(0)'><rect x='0' y='0' width='100%' height='100%' fill='hsla(0, 0%, 100%, 0)'/><path d='M40 45a5 5 0 110-10 5 5 0 010 10zM0 45a5 5 0 110-10 5 5 0 010 10zM0 5A5 5 0 110-5 5 5 0 010 5zm40 0a5 5 0 110-10 5 5 0 010 10z'  stroke-width='1' stroke='none' fill='hsla(259, 0%, 0%, 1)'/><path d='M20 25a5 5 0 110-10 5 5 0 010 10z'  stroke-width='1' stroke='none' fill='hsla(340, 0%, 0%, 1)'/></pattern></defs><rect width='800%' height='800%' transform='translate(-8,-6)' fill='url(%23a)'/></svg>");
    position: absolute;
    top: 14px;
    left: -14px;
    z-index: 1;
    border: 2px solid black;
}
```

</details>

As for the end result, it was a beautiful sight to behold. I was pleasantly surprised that it turned out to be way better looking than I thought it would be. I mean, it's like I stumbled upon a secret formula that only design wizards know of. I'll take all the credit for it, even though I have zero design skills (or so I thought).

### Continued development

- Enhance the adaptability of elements to accommodate wider screens, with a focus on optimizing the fullscreen banner
- Further explore the intricacies of utilizing SVG elements
- Refine animation and transition techniques to ensure a higher level of quality
- Expand the implementation of semantic HTML elements to improve the overall structure and accessibility of the web page.

### Useful resources

- [Кастомные чекбоксы правильно](https://www.youtube.com/watch?v=E6kLaaQFctU) - Great video abot hiding checkboxes.
- [Pattern Monster](https://pattern.monster/) - Big collection of SVG patterns
- [Shadow palette generator](https://www.joshwcomeau.com/shadow-palette/) - Perfect generator of CSS shadows

## Author

- Instagram - [@yazdrahobycha](https://instagram.com/yazdrahobycha?igshid=YmMyMTA2M2Y=)
- Telegram - [Орсен](https://t.me/yazdrahobb)

## Acknowledgments

Big thanks to [Igor4ik](https://github.com/bigheha) for support!
