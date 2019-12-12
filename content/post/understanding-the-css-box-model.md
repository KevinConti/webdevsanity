+++
aliases = []
author = "Kevin Conti"
categories = ["CSS"]
date = 2019-12-06T05:00:00Z
description = "A brief overview of the history of CSS, so we can move on to the sane stuff."
draft = true
series = ["CSS Foundations"]
tags = []
title = "Beginning CSS? Here's What You Need to Know First!"

+++
Layout:

Welcome to my **_Foundations of CSS_** free online course! After finishing these articles and completing the challenge projects found at the bottom of some of the articles, you won't be a CSS master. You won't know every nuance, and you certainly won't be ready to give a talk on the merits of various CSS architectures.

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

<p class="codepen" data-height="469" data-theme-id="default" data-default-tab="css,result" data-user="KevinConti" data-slug-hash="BayKOLV" style="height: 469px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="box model">

<span>See the Pen <a href="[https://codepen.io/KevinConti/pen/BayKOLV](https://codepen.io/KevinConti/pen/BayKOLV "https://codepen.io/KevinConti/pen/BayKOLV")">

box model</a> by Kevin Conti (<a href="[https://codepen.io/KevinConti](https://codepen.io/KevinConti "https://codepen.io/KevinConti")">@KevinConti</a>)

on <a href="[https://codepen.io](https://codepen.io "https://codepen.io")">CodePen</a>.</span>

</p>

<script async src="[https://static.codepen.io/assets/embed/ei.js](https://static.codepen.io/assets/embed/ei.js "https://static.codepen.io/assets/embed/ei.js")"></script>

**Margin**

Since this block is centered it has a large left and right margin. That's what pushes it to the center:

{{< highlight css >}}

    div {
    	margin-left: auto;
        margin-right: auto;
    }

{{< /highlight >}}

**Border**

The border for this element is that thin black line all around the block

{{< highlight css >}}

    div {
    	border: 1px solid #OD331;
        /* A border of size 1px, a solid line, 
        and a dark teal color */
    }

{{< /highlight >}}

**Padding**

The padding is the _space between the border line and the paragraph text_

{{< highlight css >}}

    div {
    	padding: 10px;
        /* Padding is 10px on all sides */
    }

{{< /highlight >}}

**Content**

The content is the size of the block. In this case, it is dynamically determined by the paragraph element inside of it.

### "So, that's great and all, but what do I need to remember about all this?"

It's confusing for beginners to understand the difference between padding and margin, but it's a simple concept once it's broken down. Margin is on the outside of the element, and padding is on the inside.

Try to keep these four terms in mind as we move on, because they will quickly become part of our shared language.

## Layout in CSS: Think of Newspaper Articles

With CSS being roughly 25 years old, it's tough for many new developers to understand the context for which it was made, myself included. This causes a mental gap if you just go through, learn the syntax, and try to apply all of this yourself. It's helpful to take a step back and remember that print media, specifically newspapers, was the dominant form of publishing at the time.

![Newspaper article from 1994](/uploads/news-article.jpg)

Looking at this article, doesn't some of it seem familiar to you in CSS terms? Do you see the h1 "Undergraduate applications set new record"? What about the black box surrounding the picture and underlying article? Doesn't that look oddly like our CSS Box Model?

The point is, when we are looking at the original layout techniques of CSS, I want you to keep this article analogy on hand, as it will help with the concepts. Some of these css techniques, such as floats, don't make sense without coming from the perspective of a newspaper article.

## The Old-Fashioned Way: The Display Property

WebDevSanity.com is all about teaching you only what you need to know about web dev, so you can reliably use it for your own projects, or work, or whatever. As such, we're only going over the critical aspects of the display property for formatting.

Why are we going over it at all, you may ask? Good question. Here's why I think it's worth discussing even though you should only use it occasionally yourself:

1. You'll see it on the web. Although you won't be implementing with it too often, it's still around, and it wouldn't be very great if there came a time where you had to at least _understand_ some CSS and it was beyond your comprehension.
2. You'll still use blocks, even with modern CSS. Even though the rest is used far less frequently, you'll still find yourself relying on good ol' **display: block** pretty frequently. As such, you better understand how it works, and you won't have a good-enough understanding unless you understand the other display options that contrast it.

With that out of the way, let's look at the basics of the **display** property

### display: There's only four values that matter

Again, we find ourselves with four values to learn. Keep in mind our newspaper article:

**display: block**

A block display is made to act like a paragraph. AKA, it is a _block_ of stuff. Block in this case means chunk, like a block of code is a chunk of code, or a block of cheese is a chunk of cheese. The div in the code example above was a block, for example.

**display: inline**

Inline is the second-most important display value out of the four. Inline displays are for when you want something to appear as _inside_ (aka inline) with another element.

For example, in newspaper articles you often see that the first letter is far bigger than the rest of the letters in the paragraph. To create this in CSS, I may do something like this:

<p class="codepen" data-height="369" data-theme-id="default" data-default-tab="css,result" data-user="KevinConti" data-slug-hash="povyxdR" style="height: 369px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="BigLetter">

<span>See the Pen <a href="[https://codepen.io/KevinConti/pen/povyxdR](https://codepen.io/KevinConti/pen/povyxdR "https://codepen.io/KevinConti/pen/povyxdR")">

BigLetter</a> by Kevin Conti (<a href="[https://codepen.io/KevinConti](https://codepen.io/KevinConti "https://codepen.io/KevinConti")">@KevinConti</a>)

on <a href="[https://codepen.io](https://codepen.io "https://codepen.io")">CodePen</a>.</span>

</p>

Notice how the 'V' is "inline" with the rest of the paragraph. Since I don't want it to effectively be inline with the paragraph, I define it as inline.

Look what happens if I define this same "V" as a block:

<p class="codepen" data-height="265" data-theme-id="default" data-default-tab="css,result" data-user="KevinConti" data-slug-hash="PowNyRo" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="BigLetter-Block">

<span>See the Pen <a href="[https://codepen.io/KevinConti/pen/PowNyRo](https://codepen.io/KevinConti/pen/PowNyRo "https://codepen.io/KevinConti/pen/PowNyRo")">

BigLetter-Block</a> by Kevin Conti (<a href="[https://codepen.io/KevinConti](https://codepen.io/KevinConti "https://codepen.io/KevinConti")">@KevinConti</a>)

on <a href="[https://codepen.io](https://codepen.io "https://codepen.io")">CodePen</a>.</span>

</p>

Notice how the V is now it's own **block**, it's own "chunk" of the page? That's the difference between block and inline.

Beginners often get confused and consider the two as interchangeable, as if they were items you apply and guess-and-check to see if it fixed your formatting issue. Now, you should understand which of the two to choose for any given element.

**display: inline-block**

Don't worry, this isn't too complicated. It's an inline element, with the added ability to define a height explicitly. Again, rarely used so I only want to mention it so you've heard of it and have an idea of what it does.

Don't think of it as a hybrid between inline and block. Think of it as inline but you can add height. It's a much better mental model.

**display: none**

The final display value we'll talk about is display: none. This entirely removes the element from the HTML. Think of this like a delete option. It's useful for when you want something to not exist on mobile devices, for example.

And that's it! Seems pretty simple, right?

## So why ignore these tools? This seems pretty straightforward.

For one, there are a host of odd bugs involved in these older layout techniques. _Floats_, which I have ignored completely for your sake, are notoriously frustrating for new developers, as they have a side-effect of taking the item in the layout out of the normal 'flow' and into it's own flow. This caused overlap issues that have had hacky solutions for years ([optional reading if you are interested](https://css-tricks.com/clearfix-a-lesson-in-web-development-evolution/)). 

Instead, here's all you need to know about old-school layout:

* it uses the 'float' and 'clear' properties to define how layout should work
* There was (and still is) a hacky solution called [Clearfix](https://css-tricks.com/clearfix-a-lesson-in-web-development-evolution/) which fixed a major layout issue.
* Modern solutions ignore float-based layouts in favor of two new strategies: Flexbox and CSS Grid.

Memorizing all of float-layouts is far too buggy for a Sane Web Dev. Unless your work requires a float based layout (browsers from before 2014), you should move on with your life.

## What's Next?

Up next, we'll dive into the holy grail of modern CSS layout, Flexbox! You'll learn the essentials of this layout platform, and we'll dive into some real examples of how to do popular website layouts. 

_Edit: The next article in this series is currently being written! Get notified when it's released by signing up for my newsletter below._ 