---
layout: post
date: 2016-05-28 16:58:00
title: 'Create an unordered list with dash bullets'
tags: 'css'
excerpt: 'Building a simple unordered list with dashes for bullets.'
---

I was building a marketing page for a client and while looking at a mockup, I came across a simple unordered, bulleted list using dashes. It's been awhile since I've written CSS consistently, so at first glance I thought that I was just going to be able to build this easily by setting the `list-style-type` property. I started to style the list however, and came to realize that dash is not a choice for `list-style-type`.

## list-style-image

Just kidding... No but seriously, this was where my mind went initially, cause it's been that long since the last time I needed to create a custom bullet. It's safe to say though, that this should never be the course

## CSS content

I *quickly* correctly my last train of thought and decided to use CSS's `content` property.

<iframe width="100%" height="300" src="//jsfiddle.net/codfish/gck6hL1o/embedded/css/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

You could also use an en dash or em dash if you wanted a wider bullet. If you want to do that you'll need to use the unicode for those characters.

- en dash: `content: '\2013'`
- em dash: `content: '\2014'`

You'll probably need to adjust the left padding on the line items if you use one of these wider-than-dash characters.

## Aligning the dash

Notice that both the line items and their `:before` content receive the same `line-height`, and more importantly, it's set in `rem`'s ([snook.ca's explanation of rem's](http://snook.ca/archives/html_and_css/font-size-with-rem)). You can change the value to whatever you like, just always use `rem` units.

```css
.dashed-list {
  line-height: 2rem;
}
```

That's important because we want to make sure they're exactly the same, regardless of the font size of the `li`'s and the dashes. This guarantees us some flexibility to change the size of the line items, while keeping the dashes vertically aligned.

## Positioning

In order to get the dashes showing up in the right spot, I'm using absolute positioning. I originally tried messing around with negative margins, but I noticed the dash wasn't vertically centered with the `li`'s first line, so I felt positioning would give me a greater amount of control.

First step is to give the li's some left padding cause we need room for the dash to live. Then we'll set `position: relative` on the `li` to allow us to position those dashes absolutely. Then we can set a left position of 0, and to help us with centering the dash, a small negative margin of `-1em`. If you decide you want bigger dashes and increase their `font-size`, using em's on that negative margin will keep them centered nicely.

## The final result

<iframe width="100%" height="300" src="//jsfiddle.net/codfish/gck6hL1o/embedded/result,css,html" allowfullscreen="allowfullscreen" frameborder="0"></iframe>
