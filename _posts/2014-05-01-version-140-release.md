---
layout: post
title: "Version 1.4.0 released!"
description: "Version 1.4.0 of under-os was just released!"
category: ""
tags: ["release"]
---
{% include JB/setup %}

Greetings my dear friends, as I have great news for you today! Our beloved under-os was just bumped to the next version!

## Change #1

There are many changes, but the most important change of all is that starting from this version the `under-os` gem
is getting split into three

1. `under-os-core` - has the bootloader and the core functionality
2. `under-os-ui` - has all the UI related code (pages, html, css and ui events)
3. `under-os-http` - contains the nice, ruby like HTTP wrapper

The main `under-os` gem is still out there it just now it is a shallow gem that includes those three as dependencies. So, all your old code should be working fine, but now you have options to include only what you need into your project.

The reason why we do that is not just the obvious reducing the complexity and enabling modularity. One of the goals of this project is not to just create a "thing", but rather create an infrastructure to build things. We are breaking things apart and eating our own dog food to enable under-os to be easily extended much in the ruby community way.

Such ruby! Many gems!

## Other Changes

1. the `UI::Events::Event` class received several new methods related to handling touch gesture recognizers. Those include things like `#scale`, `#angle` and `#translation`
2. the `UI::Scroll` class was extended with quite a few new methods to help you work with scaling and panning. Now you have such methods as `#scale`, `#contentOffset` and so on. The scroller also received several patches here and there to address issues with handling the `overflow` styles.
3. the `UOS::Point` unit is now mutable. It also has two new fancy methods `#+` and `#-` to help you to deal with two dimensional calculations. It's pretty handy when you need to say calculate cumulative offsets and such.
4. the CSS processor now understand the `font-family` and `font-style` properties.
5. minor bug fixes and performance optimizations.

And that's about it. Enjoy, and I'll see you around!
