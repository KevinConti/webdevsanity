+++
aliases = []
author = "Kevin Conti"
categories = ["CSS"]
date = 2019-12-06T05:00:00Z
description = "A brief overview of the history of CSS, so we can move on to the sane stuff."
draft = true
series = ["CSS Foundations"]
tags = []
title = "Where to Begin With CSS? The Display Property"

+++
Layout:

Welcome to my _Foundations of CSS_ free online course! After finishing these articles and completing the challenge projects found at the bottom of some of the articles, you won't be a CSS master. You won't know every nuance, and you certainly won't be ready to give a talk on the merits of various CSS architectures.

Instead, you'll know how to quickly and reliably create the exact layout you want within CSS, in plain, no-bs language.

What do I expect from you before you take this course?

* You should already know basic CSS syntax. If you don't, [learn it here. ](https://www.w3schools.com/css/css_syntax.asp "w3schools")
* You are willing to learn by doing, and will complete the exercises in the course when they appear.

If the above doesn't apply to you, please look elsewhere.

***

In this article, you will learn...

* What the CSS box model is, and why it's important
* Why CSS should make you think of newspaper articles
* The old way of layout: Display property (and why you don't need to master it)
* A primer on the new/better way of layout

## The CSS Box Model

The CSS Box Model is just a fancy way of saying that all CSS elements are "boxes", even if they don't look like them. When we talk about the space between elements, we need to know the four parts of the CSS Box Model:

![CSS Box Model](/uploads/Group 1.png "CSS Box Model")

1. Margin - The space around a box
2. Border - The box itself - the edge of the element
3. Padding - the white space between the border and any content
4. Content - the insides of the box

It's easiest to see this with a real example. Let's look at a paragraph:

<p class="codepen" data-height="265" data-theme-id="default" data-default-tab="css,result" data-user="KevinConti" data-slug-hash="BayKOLV" style="height: 800px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="box model">   <span>See the Pen <a href="https://codepen.io/KevinConti/pen/BayKOLV">   box model</a> by Kevin Conti (<a href="https://codepen.io/KevinConti">@KevinConti</a>)   on <a href="https://codepen.io">CodePen</a>.</span> </p> <script async src="https://static.codepen.io/assets/embed/ei.js"></script>

* Primer on Box Model (very quick!) - code pen
* Analagy: Newspaper articles
  * When CSS was being designed, newspaper (and print media in general) was the primary source of content. CSS is modeled after this style, and it is important to keep that in mind.
* Display: none, block, inline
  * block is made to act like a paragraph, AKA it is it's own content
  * inline is made to be part of a paragraph, AKA a line inside a block
  * none is made to entirely hide the content
* Why is it so confusing when I go to make my own layouts?
  * Just like in newspapers, block elements do not always take up the whole line (can have width specified) - code pen
  * Inline values can have horizontal margin in order to be bigger than their elements - code pen
* inline-block:
  * Newspaper, think of it as an inline element (goes inside a paragraph), but it is itself a block. Think of when print articles have a big first letter and the rest of the paragraph is normal - code-snippet
* Why a Sane Web Dev doesn't prefer these tools anymore
  * Better things have been implemented in CSS for layout: flexbox and CSS grid
  * Lots of bugs, with hacks required - code pens I already wrote
  * Memorizing all this is too hard. More important for you is to understand the concepts, especially blocks, and then move on with your life

> Notes:
>
> What makes up a box? Content -> padding -> border -> margin
>
> There are default styles for elements assigned by the browser, just because you didn't set them doesn't mean there isn't something going on
>
> CSS elements prefer to place themselves left to right, and only go to a new line if there isn't free space
>
> display:
>
> none - removed from the html page entirely
>
> block - takes up all space horizontally
>
> inline - only as wide as their content
>
> Why it's so confusing:
>
> block values can have width: 50% to look like inline values
>
> inline values can have margin to make them wider than their contents
>
> (need to prove this to myself via example)
>
> inline-block - rarely used, but main difference is that it can have vertical emphasis
>
> auto?
>
> \*_inline vs inline-block elements are affected by whitespace inside your html_*
>
> \*_inline-block default is not border-box, meaning that if you have a border the spacing will be fucked up_*