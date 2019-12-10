+++
aliases = []
author = "Kevin Conti"
categories = ["CSS"]
date = 2019-12-06T05:00:00Z
description = "A brief overview of the history of CSS, so we can move on to the sane stuff."
draft = true
series = ["CSS Foundations"]
tags = []
title = "The Display Property (CSS Foundations - 1)"

+++
Notes go here: 

What makes up a box? Content -> padding -> border -> margin

There are default styles for elements assigned by the browser, just because you didn't set them doesn't mean there isn't something going on

CSS elements prefer to place themselves left to right, and only go to a new line if there isn't free space

display:

none - removed from the html page entirely

block - takes up all space horizontally

inline - only as wide as their content

Why it's so confusing:

block values can have width: 50% to look like inline values

inline values can have margin to make them wider than their contents

(need to prove this to myself via example)

inline-block - rarely used, but main difference is that it can have vertical emphasis

auto?

\**inline vs inline-block elements are affected by whitespace inside your html**

\**inline-block default is not border-box, meaning that if you have a border the spacing will be fucked up**