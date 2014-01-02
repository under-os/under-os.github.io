---
layout: post
title: "Version 1.2.0 is out"
description: "The new version of under-os 1.2.0 is out!"
category: ""
tags: ["release"]
---
{% include JB/setup %}

Hey my dear friends, while the xmas break is still on, we have one more
under-os release!

This time we're filling in the blanks in the input fields and forms.

### New Tag `FORM`

The new tag `FORM` was added. We don't really have things like URLs
and actions in native development, but forms are still great way to
organize and deal with input fields. So, uOS now has the `FORM` tag

    <form id="signin">
      <input type="text" name="username" />
      <input type="password" name="password" />
    </form>

And as you would expect the `UOS::UI::Form` instances provide you with
the usual `#inputs` and `#values` methods

    u('form#signin').inputs # -> [input, input]
    u('form#signin').values # -> {'username' => 'smth', 'password' => 'smth'}


### UI::Input Types Support

The `INPUT` tags now have proper support of the `type` property, so you can say
the usual

    <input type="text" name="username" />
    <input type="password" name="password" />

But there is also a few extra types that are relevant to native mobile development,
like for example `phone`, `email`, `url`, `search`, etc.

All those types are automatically translated into the native iOS input fields
keyboard settings and will show the appropriate keyboard when the user interacts
with those fields.

### UI::Input `#disabled`, `#focus`, `#blur` Support

All the input fields now also support the usual for web-development API that
allow you to set and query the state of the fields programmatically.
It looks just like you would expect it

    u('#my-input').disabled = true
    u('#something-else').focus


### UI::Input `focus`, `blur`, `change` Events Support

All the input fields (including textareas, selectboxes, sliders and switches)
now properly support the `focus`, `blur` and `change` events, the same exact
way we have it in the browsers

    u('#search').on(:blur) { trigger_search }
    u('#switch').on(:change) { trigger_some_logic }

### The Attribute CSS Selectors Support

The css selectors engine now supports the CSS3 attributes matching queries,
works just as you would expect it

    u('input[type=text]') # all inputs with type="text"
    u('input[type=password]') # all password fields

### `VIEW` -> `DIV` Alias

All the view elements in uOS are inherited from the `UI::View` class and you
can always use the `VIEW` tag in your layouts when you just need a block element,
but the old habbits die hard, and it's not really obvious that we have the `VIEW`
tag instead of the usual `DIV`'s, so starting with the version `1.2.0`, we have
the `DIV` tag as well.


---

And that all we've got for this release. Enjoy!
