---
layout:     default
title:      Styling with Sass
date:       2020-10-26
category:   Posts Coding Sass
author:     Jordan 
permalink:  bamboo-horseshoe
---


## As I hope you can tell, I have finally gotten around to learning some web development and have gotten pretty good with CSS (using Sass) over this past week if I do say so myself (did you hit that toggle in the header and see the transition to my high readability/dark mode yet?).


After quite a bit of research into the various languages and softwares for web development, watching videos to get a feel for what you can achieve with each, what they're generally used for, how commonly they're used in the businesses that I want to hire me etc, I decided that CSS would be the best language for me to start with and it just so happened that CSS was exactly what the template for this blog was made with! Pretty lucky there as it meant that I already had a nice, functional website that I could play with and really start understanding what various elements of it do just by going through what I already had and I didn't have to make a new website from scratch. It's actually been really fun to just get stuck in with it, hasn't been so great for my sleeping pattern or cooking proper meals as I've typically been so completely absorbed by whatever task was at hand that by the time I realise that I'm hungry, I am HUNGRY and don't particularly fancy the wait time until what I'd planned to eat was all chopped and cooked and I'm actually quite hungry right now so I'm gonna stop talking about food and get on with what this post is about.

To really make the most out of what I could learn with this blog, I wanted to customise as much of it as I could think to, starting with the colour scheme. This actually lead into much longer searching for and editing photos than I'd like to admit, this wave background was like the third picture I chose for the background of the header (before I decided it was a bit much and just went for a solid colour header) and this must be at least the 5th "finished" edit of it, the first 3 were actually the other way up. Once I'd finally settled on the image and reduced it's saturation enough that you could actually read the text over it, I had to position it. This turned out to be significantly harder than expected with the `height` and `width` parameters as each page was a different size depending on how long the blog was. Eventually, I found out that you could also use `min-height` and `min-width` parameters along with a `background-size: cover` and `background-repeat: no repeat` rule that would automatically rescale (not replicate) the image to cover the page. Using VS Code for this was also a huge help as I was able to install extensions that mean when you hover over a parameter it gives the available options and Google can explain what they mean; plus it opens up a visual colour and transparency selector when you hover over a colour code, which makes it significantly easier to get the shades you want than by experimenting with rgba values.

I still don't really understand how to properly work with the `float` and `position` elements to get things where I want, but with a small amount of trial and error and the [w3schools](https://www.w3schools.com/cssref/pr_class_float.asp) pages that give definitions, examples and let you test different options I've been able to get the layout how I want without too much trouble. I also used the interactive services on that site to format the `border-radius` to shape the coloured background around this text and the sidebar which was really useful, there are quite a few useful sites though and I generally just search something like 'CSS border shape' and see what comes up. I also used a few YouTube tutorials for things like this [tutorial](https://www.youtube.com/watch?v=ZKXv_ZHQ654) for the theme toggle. I like to at least have an idea of what something does before I do it so that I can try and set it up how I want it in the first place rather than going back through every aspect after, so when I'm doing something completely new I find it handy to have a video that I can watch through to build a bit of understanding and then watch it again while following along. Other than adding functionality to the blog and making it more accessible for people with visual impairments (I also found out that that is a reason to include an `alt` on every image even if it has a `title`), adding the high readability theme was a good way to solidify what I'd learnt so far as it meant going back through the whole SCSS file to see what I wanted to change and then refining the values for the new theme.

Obviously I haven't mastered CSS in the week I've been using it, but I am very happy with how much I've progressed and how much I feel I understand after such a short time, I'm looking at learning PHP next and building a page for my online portfolio from scratch next.

I don't know if it's just me, but the last few days I've really been noticing how colourful and pretty the clouds look, I feel like they have a lot more reds, blues and purples than I've ever noticed before, I've always just thought clouds are white or grey.

Stay safe, appreciate nature and I'll see next time,

¡JaBlog!

[back](./)
