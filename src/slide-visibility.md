---
id: slide-visibility
title: Slide Visibility
layout: default
---

# Slide Visibility
The `data-visibility` attribute can be used to hide slides. It can also be used to mark slides as "uncounted" in reveal.js' internal numbering system, which affects the visible slide number and progress bar.

## Hidden Slides <span class="r-version-badge new">4.1.0</span>

To hide a slide from view, add `data-visibility="hidden"`. Hidden slides are removed from the DOM as soon as reveal.js is initialized.

```html
<section>Slide 1</section>
<section data-visibility="hidden">Slide 2</section>
<section>Slide 3</section>
```
<div class="reveal reveal-example" data-config='{"slideNumber": "c/t"}'>
  <div class="slides">
    <section>Slide 1</section>
    <section data-visibility="hidden">Slide 2</section>
    <section>Slide 3</section>
  </div>
</div>

## Uncounted Slides

When preparing a presentation it can sometimes be helpful to prepare optional slides that you may or may not have time to show. This is easily done by appending a few slides at the end of the presentation, however this means that the reveal.js progress bar and slide numbering will hint that there are additional slides.

To "hide" those slides from reveal.js' numbering system you can use `data-visibility="uncounted"`.

**Note:** This only works for slides at the end of the presentation, after all of your main slides.

```html
<section>Slide 1</section>
<section>Slide 2</section>
<section data-visibility="uncounted">Slide 3</section>
```
<div class="reveal reveal-example" data-config='{"slideNumber": "c/t", "progress": true}'>
  <div class="slides">
    <section>Slide 1</section>
    <section>Slide 2</section>
    <section data-visibility="uncounted">Slide 3</section>
  </div>
</div>

