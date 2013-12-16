---
layout: page
tagline: Supporting tagline
---
{% include JB/setup %}

While HTML5 vs. Native folks call each other mom names, we build the future!

## iOS app in 10 minutes

<iframe src="http://player.vimeo.com/video/81919125" width="100%" height="388" frameborder="0" allowfullscreen="true"> </iframe>
<br/>

## What's That?

`UnderOS` (or shortly `uOS`) is a project that aims to build a web-browser like
environment on top of <a href="http://www.rubymotion.com">RubyMotion</a> so you
could build native iOS apps while keeping your web-developer's habbits.


## Getting Started

Assuming you've got <a href="http://www.rubymotion.com">RubyMotion</a> installed.

1) Install the `under-os` rubygem

    gem install under-os

2) Clone the `uos` rubymotion template in your system

    mkdir -p ~/Library/RubyMotion/template/uos
    git clone https://github.com/under-os/under-os-template.git ~/Library/RubyMotion/template/uos

3) Generate a new project using the `uos` template

    motion create test --template=uos

Now just go there and run it!

    cd test && rake

Enjoy!

## Give Me Moar!

There are plenty of various examples at the `under-os` main repo

    git clone https://github.com/under-os/under-os.git
    cd under-os
    rake

See the `app/` folder, it contains all the examples


## Contacts

Please feel free to shoot me a message <a href="https://twitter.com/nemshilov">@nemshilov</a>
or <a href="https://twitter.com/under_os">@under_os</a>

You also can post feature requests and issues on the
<a href="https://github.com/under-os/under-os/issues">GitHub issues list</a>
