# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### Screenshot

![Recipe-page](https://github.com/user-attachments/assets/6671fa16-d559-441b-b8cd-c7962d4bf723)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- SCSS
- Flexbox
- CSS Grid
- BEM Notation

### What I learned

Utility Classes and Tailwind: Discovered that Tailwind CSS is essentially a collection of utility classes that you can also create in regular CSS.
Styling Bullet Points: Learned to use &::marker in SCSS to change the color of bullet points in lists.
Bullet Points Positioning: Noted that by default, bullet points in a <ul> are outside the element, but using list-style-position: inside; can keep them inside the element.
Best Practices for @font-face: Learned not to add properties like letter-spacing, font-size, or line-height in @font-face; only use properties like font-weight.
Default Styles for Headings: Realized that the h2 tag has a default font-weight of bold, which can affect the thickness of the text.
Using '<span>' for Spacing: Found that span elements can be used to create gaps between bullet points and text in a list.
Challenges with list-style-position: inside;: Experienced issues with number alignment and text when using list-style-position: inside;.
Working with Tables: Began using tables for better accessibility and struggled with styling them precisely.
Styling Tables: Faced challenges in getting the table to look exactly as intended

To see how you can add code snippets, see below:

```html
<table class="card__nutrition">
          <caption class="card__nutrition-title">
            Nutrition
          </caption>

          <thead class="card__nutrition-sub">
            <th>
              The table below shows nutritional values per serving without the
              additional fillings.
            </th>
          </thead>

          <tbody class="card__nutrition-list">
            <tr class="card__nutrition-item">
              <th>Calories</th>
              <td>277kcal</td>
            </tr>

            <tr class="card__nutrition-item">
              <th>Carbs</th>
              <td>0g</td>
            </tr>

            <tr class="card__nutrition-item">
              <th>Protein</th>
              <td>20g</td>
            </tr>

            <tr class="card__nutrition-item">
              <th>Fat</th>
              <td>22g</td>
            </tr>
          </tbody>
        </table>
```
```css
&__nutrition {
        @include mixins.layout(grid, spacing.$spacing-300);

        &-title {
            font-size: 28px;
            text-align: left;
            @include mixins.text-preset("young-serif", 100%, 0, variable.$brown80, normal);
        }
        &-sub th {
            font-size: 16px;
            @include mixins.text-preset("outfit-regular", 150%, 0, variable.$stone60, normal);
        }
        &-item {
            @include mixins.text-preset("outfit-regular", 150%, 0, variable.$stone60, normal);
            font-size: 16px;
            display: flex;
            justify-content: space-around;
            text-align: left;
            border-bottom: 1px solid variable.$stone15;
            padding: 0 spacing.$spacing-400 0 spacing.$spacing-400;
        }
        &-item th {
            font-weight: normal;
            width: 100%;
        }
        &-item td {
            @include mixins.text-preset("outfit-bold", 150%, 0, variable.$brown80, null);
            width: 100%;
            margin-left: spacing.$spacing-200;
        }
        &-item:nth-child(1),
        &-item:nth-child(2),
        &-item:nth-child(3) {
            padding-bottom: spacing.$spacing-150;
        }
        &-item:nth-child(2),
        &-item:nth-child(3),
        &-item:nth-child(4) {
            padding-top: spacing.$spacing-150;
        }
        &-item:nth-child(4) {
            border: transparent;
        }
    }
}
```
