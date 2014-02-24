---
layout: post
title: "Version 1.3.0 released!"
description: "The new version of under-os was just released!"
category: ""
tags: ["release"]
---
{% include JB/setup %}

Hey folks, how are going? I've got some great news for you today,
the version 1.3.0 of our world famous `under-os` project was just released!

There are two major new features and a few small fixes/updates

### The New Extensions API

One of the goals of uOS is that I want an easily extensible system, so
today I'm releasing the new, small but smarty-pantsy, one method API for
extending UnderOS with your hot awesomeness. It looks like that

    UOS.extend __FILE__

Yup. That's it. Well, not really, but the idea is that whenever you write
a plugin for `UnderOS`, you should call that method from your main file in
the `lib/` folder of your plugin. Once you've done that, `UOS` will automatically
inject all your code and assets into the project.

UnderOS itself is actually built on top of this feature,
[check this out](https://github.com/under-os/under-os/blob/master/lib/under-os.rb)!

### Touch Events Support

Another major change is that now we support the `touchstart`, `touchend` and
`touchmove` events the same way they work in the browsers.

From the beginning `UOS` was shipped with the basic gesture recognitions mapping,
so could easily watch for taps and swipes, but, in many cases you actually
need the raw touch start/move/stop events. Now you have them!

    find('#my-view').on :touchstart do |event|
      puts event.touches[0].pageX
    end

It all looks pretty much like normal W3C events, so you can just start using them.


### Fixes & Small Features

 * `box-shadow` and `text-shadow` CSS styles are now properly mapped to
   native properties and available to use in stylesheets.

 * The `navbar` object now has the `enable_swipes`, `disable_swipes`
   methods so you could control whether the user should be able to use
   the iOS7 swipes navigation or not (useful when you have drag-n-drop
   elements on a page).

 * The `History#current_page` method now returns the correct current
   page object in case of modal views being presented on top of it.


And that's the whole list. Enjoy, build awesome stuff, stay cool!

-- Nikolay

