# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![Design screenshot](https://github.com/TheCoder-Rahul/fontend_mentor_testimonials_grid/blob/main/project_screenshot.png)


### Links

- 👉 [Solution URL](https://github.com/TheCoder-Rahul/fontend_mentor_testimonials_grid.git)
- 👉 [Live Site URL](https://thecoder-rahul.github.io/fontend_mentor_testimonials_grid/)

## My process

### Built with

- 👉 **Markup:** Semantic HTML5 for better accessibility and SEO.
- 👉 **Styling:** CSS3 with Custom Properties (variables) for a maintainable color scheme, font-properties, and different sizes.
- 👉 **Layout:** CSS Grid (Grid Template Areas) for the main layout and Flexbox for internal component alignment.
- 👉 **Workflow:** Mobile-first approach and Responsive Design using Media Queries.

### What I learned

**Mastering Complex Layouts with CSS Grid**

In this project, I gained a deeper understanding of the grid-template-areas property. It allowed me to map out the asymmetrical testimonial sections visually in my CSS, making the transition from a single-column mobile view to a complex 4-column desktop grid much more intuitive and readable.

Check my code snippets below:

```html
<main class="container">
  <article class="testimonial_1">
    <img class="quotation_mark" src="images/bg-pattern-quotation.svg" alt="Quotation Mark Icon" aria-hidden="true">
    <section class="testimonial_profile">
      <img src="./images/image-daniel.jpg" alt="Daniel Clifford Profile Image">
      <div class="testimonial_info">
        <h3>Daniel Clifford</h3>
        <p>Verified Graduate</p>
      </div>
    </section>
    <h2 class="testimonial_title">I received a job offer mid-course, and the subjects I learned were current, if not more so, in the company I joined. I honestly feel I got every penny's worth.</h2>
    <p class="testimonial_text">“ I was an EMT for many years before I joined the bootcamp. I've been looking to make a transition and have heard some people who had an amazing experience here. I signed up for the free intro course and found it incredibly fun! I enrolled shortly thereafter. The next 12 weeks was the best - and most grueling - time of my life. Since completing the course, I've successfully switched careers, working as a Software Engineer at a VR startup. ”</p>
  </article>
  <article class="testimonial_2">
    <section class="testimonial_profile">
      <img src="./images/image-jonathan.jpg" alt="Jonathan Walters Profile Image">
      <div class="testimonial_info">
        <h3>Jonathan Walters</h3>
        <p>Verified Graduate</p>
      </div>
    </section>
    <h2 class="testimonial_title">The team was very supportive and kept me motivated</h2>
    <p class="testimonial_text">“ I started as a total newbie with virtually no coding skills. I now work as a mobile engineer at a big company. This was one of the best investments I've made in myself. ”</p>
  </article>
  <article class="testimonial_3">
    <section class="testimonial_profile">
      <img src="./images/image-jeanette.jpg" alt="Jeanette Harmon Profile Image">
      <div class="testimonial_info">
        <h3>Jeanette Harmon</h3>
        <p>Verified Graduate</p>
      </div>
    </section>
    <h2 class="testimonial_title">An overall wonderful and rewarding experience</h2>
    <p class="testimonial_text">“ Thank you for the wonderful experience! I now have a job I really enjoy, and make a good living 
  while doing something I love. ”</p>
  </article>
  <article class="testimonial_4">
    <section class="testimonial_profile">
      <img src="./images/image-patrick.jpg" alt="Patrick Abrams Profile Image">
      <div class="testimonial_info">
        <h3>Patrick Abrams</h3>
        <p>Verified Graduate</p>
      </div>
    </section>
    <h2 class="testimonial_title">Awesome teaching support from TAs who did the bootcamp themselves. Getting guidance from them and learning from their experiences was easy.</h2>
    <p class="testimonial_text">“ The staff seem genuinely concerned about my progress which I find really refreshing. The program gave me the confidence necessary to be able to go out in the world and present myself as a capable junior developer. The standard is above the rest. You will get the personal attention you need from an incredible community of smart and amazing people. ”</p>
  </article>
  <article class="testimonial_5">
    <section class="testimonial_profile">
      <img src="./images/image-kira.jpg" alt="Kira Whittle Profile Image">
      <div class="testimonial_info">
        <h3>Kira Whittle</h3>
        <p>Verified Graduate</p>
      </div>
    </section>
    <h2 class="testimonial_title">Such a life-changing experience. Highly recommended!</h2>
    <p class="testimonial_text">“ Before joining the bootcamp, I've never written a line of code. I needed some structure from professionals who can help me learn programming step by step. I was encouraged to enroll by a former student of theirs who can only say wonderful things about the program. The entire curriculum and staff did not disappoint. They were very hands-on and I never had to wait long for assistance. The agile team project, in particular, was outstanding. It took my learning to the next level in a way that no tutorial could ever have. In fact, I've often referred to it during interviews as an example of my developent experience. It certainly helped me land a job as a full-stack developer after receiving multiple offers. 100% recommend! ”</p>
  </article>
</main>
```
```css
@font-face {
  font-family: 'Barlow';
  src: url('./fonts/BarlowSemiCondensed-Medium.ttf') format('truetype');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Barlow';
  src: url('./fonts/BarlowSemiCondensed-SemiBold.ttf') format('truetype');
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}
:root {
  --body-font: 0.813rem;
  --small-font: 0.75rem;
  --headings-font: 1.25rem;
  --sec-headings-font: 0.9rem;
  --medium-weight-font: 500;
  --semibold-weight-font: 600;
  --black: hsl(0, 0%, 7%);
  --white: hsl(0, 0%, 100%);
  --grey-200: hsl(0, 0%, 81%);
  --grey-100: hsl(214, 17%, 92%);
  --grey-400: hsl(224, 10%, 45%);
  --grey-500: hsl(217, 19%, 35%);
  --dark-blue: hsl(219, 29%, 14%);
  --purple-50: hsl(260, 100%, 95%);
  --purple-300: hsl(264, 82%, 80%);
  --purple-500: hsl(263, 55%, 52%);
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  line-height: 1.2;
  font-size: var(--body-font);
  background-color: var(--grey-100);
  font-family: 'Barlow', sans-serif;
  font-weight: var(--medium-weight-font);
}
.container {
  gap: 2rem;
  display: grid;
  margin: 0 auto;
  max-width: 70rem;
  padding: 4rem 2rem;
}
article {
  gap: 1.5rem;
  display: flex;
  padding: 2rem;
  flex-direction: column;
  border-radius: 0.5rem;
  background-color: var(--white);
  box-shadow: 2rem 2rem 4rem hsla(224, 10%, 45%, 0.25);
}
.testimonial_1 {
  position: relative;
  --border-clr: var(--purple-300);
  --info-text-clr: var(--grey-100);
  --info-header-clr: var(--grey-100);
  background-color: var(--purple-500);
  --testimonial-text-clr: var(--grey-100);
  --testimonial-title-clr: var(--grey-100);
}
.testimonial_1 .quotation_mark {
  z-index: 1;
  position: absolute;
  inset: 0 3rem auto auto;
}
.testimonial_1 > * {
  z-index: 2;
  position: relative;
}
.testimonial_2 {
  --border-clr: var(--grey-500);
  --info-text-clr: var(--grey-100);
  --info-header-clr: var(--grey-100);
  background-color: var(--grey-500);
  --testimonial-text-clr: var(--grey-100);
  --testimonial-title-clr: var(--grey-100);
}
.testimonial_3, .testimonial_5 {
  --border-clr: var(--white);
  --info-text-clr: var(--grey-400);
  --info-header-clr: var(--grey-500);
  background-color: var(--white);
  --testimonial-text-clr: var(--grey-400);
  --testimonial-title-clr: var(--grey-500);
}
.testimonial_4 {
  --border-clr: var(--purple-300);
  --info-text-clr: var(--white);
  --info-header-clr: var(--white);
  background-color: var(--dark-blue);
  --testimonial-text-clr: var(--white);
  --testimonial-title-clr: var(--white);
}
.testimonial_profile {
  gap: 1rem;
  display: flex;
  align-items: center;
}
.testimonial_profile img {
  width: 2rem;
  height: 2rem;
  border-radius: 50%;
  border: 0.125rem solid var(--border-clr);
}
.testimonial_info h3 {
  color: var(--info-header-clr);
  font-size: var(--sec-headings-font);
  font-weight: var(--semibold-weight-font);
}
.testimonial_info p {
  color: var(--info-text-clr);
  font-size: var(--small-font);
  font-weight: var(--medium-weight-font);
}
.testimonial_title {
  color: var(--testimonial-title-clr);
  font-size: var(--headings-font);
  font-weight: var(--semibold-weight-font);
}
.testimonial_text {
  line-height: 1.5;
  color: var(--testimonial-text-clr);
}
.attribution { font-size: 11px; text-align: center; position: absolute; bottom: 1rem; }
.attribution a { color: var(--purple-500); }

@media (min-width: 768px) {
  body {
    height: 100vh;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
  }
  .container {
    padding: 0;
    row-gap: 1.5rem;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: minmax(auto, 1fr);
    grid-template-areas: 'testimonial_1 testimonial_1 testimonial_2 testimonial_5'
                         'testimonial_3 testimonial_4 testimonial_4 testimonial_5';
  }
  .testimonial_1 { grid-area: testimonial_1; }
  .testimonial_2 { grid-area: testimonial_2; }
  .testimonial_3 { grid-area: testimonial_3; }
  .testimonial_4 { grid-area: testimonial_4; }
  .testimonial_5 { grid-area: testimonial_5; }
}
```

## Author

- 👉 GitHub - [TheCoder-Rahul](https://github.com/TheCoder-Rahul)
- 👉 Frontend Mentor - [@TheCoder-Rahul](https://www.frontendmentor.io/profile/TheCoder-Rahul)
- 👉 LinkedIn - [@Rahul Kumar](https://www.linkedin.com/in/rahul-the-developer/)