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

* Before: Intro to Series link
* Introduction: why you are learning this first
  * What you will learn
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
> \**inline vs inline-block elements are affected by whitespace inside your html**
>
> \**inline-block default is not border-box, meaning that if you have a border the spacing will be fucked up**