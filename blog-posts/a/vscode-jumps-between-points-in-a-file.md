---
published: false
title: "Your title"
cover_image: "https://raw.githubusercontent.com/YOUR-USERNAME/YOUR-REPO/master/blog-posts/NAME-OF-YOUR-BLOG-POST/assets/your-asset.png"
description: "Description of the article"
tags: tag1, tag2, tag3
series:
canonical_url:
---



# VSCode - How to Jumps between Points in a File
# marson test

This article contains tips to jumps between points (combination of line & column number) in a single file 
in VSCode for screen reader users (blind, visuallly impaired, etc).
This article is based on personal experience.

## Background

I often face situation where I have to jumps from 1 point to another line back and forth in a single file. It is a bit challenging for me since now I am a screen reader user. 

As an example, in JSON file below I need to look for `sku`s in `products` to replace `sku` (xxx) in the `cart` array.  
Imagine scenarios with much more products and more cart items.
It will require me to traverse through the `products` for each `cart` item.

{% embed https://gist.github.com/wiscer-org/48f2077ad3c3c2310a8006e5134db578 %}

## Sighted Users
This is how a sighted user will complete the task :
1. Get the  `name` of the first `cart` item.
2. Scroll to `products`.
3. Traverse through the `products` until find the matching `name`.
4. Remember the `sku`.
5. Scroll back to the first item of `cart`.
6. Replace `xxx` with the `sku`.
7. Repeat from the beginning for the second item in `cart`.

The steps above are pretty simple because a sighted user only need to scroll down/up without having to repeatedly press keys to navigate.

## Screen Reader Users

Screen reader (SC) users, on the other hand, do not use scrollable devices.
They only use keyboards to give input to computer.
SC users have to press key up / down to replace the 'scrolling' done by sighted users.
During the navigation process, SC users have to press up/down key to move cursor 1 line to read each line until reaching the intended 'section'.
It will require much longer time to complete simple task such as above, compared to sighted users.

Below are tips I used to  workaround the challenge.
Let's consider an initial condition for each tips
where the cursor is at `"name" : "Milk"` (line 4).

### Use `PgUp` and `PgDown` keys



### Use line numbers

### Find 'dummy' anchors

### Use multiple editor.

