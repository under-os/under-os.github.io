---
layout: post
title: "Version 1.1.0 is out"
description: "The new version of under-os 1.1.0 is out!"
category: ""
tags: ["release"]
---
{% include JB/setup %}

My dear fellow programmers, it is with a light heart i announce that
the new version of our beloved under-os was just released.

It was rather quick, but this is how we're going to roll them out,
the shortest cycle possible, one feature at the time, no 6 months
waiting period, as soon as we have it we ship it.

So, today's realease brings us the `HTTP` stack. It was outlined
before, but now we've finally filled the blanks in and it's ready
to rock. Generally it looks like that.

    UOS::HTTP.get "http://google.com" do |response|
      puts response.body
    end

If you ever done any `ajax` (and who didn't) then you'll feel right
at home, the deal is pretty much the same, you specify url and params
and get a response in a callback. You can `GET`, `POST`, `PUT` and
the rest of the stuff pretty much the usual way.

Plus we've got a bunch of useful tools to work with JSON, namely
the `JSON` module

    UOS::HTTP.get "/search.json?q=puppy" do |response|
      puts JSON.parse(response.body)
    end

Or you can just say `response.json`, that will work too.

And finally you've got hooks to load images, which in case of
native development might be a bit tricky, so we make it simpler
for you

    u('#my-image').load "http://smth.com/image.jpg"

Just like that.

Enjoy, and merry xmas to you all!
