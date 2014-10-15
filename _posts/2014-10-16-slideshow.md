---
title     : Bootstrap Slideshow
layout    : post
category  : hands-on
tagline   : Implementing a slideshow (or carousel) in Bootstrap.
tags      : [week07, review, html, bootstrap, slideshow]

---

{% include JB/setup %}

[Bootstrap](http://getbootstrap.com) comes with a built in [carousel](http://getbootstrap.com/javascript/#carousel-usage) feature. Bootstrap's carousel is by no means the only way you can make a slide show on a web page, but it is what we're going to use this semester.  The feature is fairly [well documented](http://getbootstrap.com/javascript/#carousel-usage) but the documentation is a bit terse for beginners. Tutorial Republic has a [more thorough walk-through](http://www.tutorialrepublic.com/twitter-bootstrap-tutorial/bootstrap-carousel.php) that you may find helpful. 

I have put together a super basic jQuery slideshow using the Twitter Bootstrap:

+ [Slideshow Template](https://github.com/amandabee/cunyjdata/blob/master/lecture%20notes/bootstrap/basic_bootstrap_with_slides.html)

There are a lot of moving pieces here and they provide a lovely opportunity to introduce the [DOM](https://en.wikipedia.org/wiki/Document_Object_Model). The easiest way to think about this concept is that your HTML page is a collection of "objects" (which in a way it is) like boxes and paragraphs. And if you want scripts to act on just one "object" you need to identify it. There are many women in this room, but I'm the only "Amanda Hickman". There are many `<div>`s on this page but when I say this one is to be a slider, well ...

What that means for us is that your carousel lives in a `<div ...>` and that div has a unique `id` -- an attribute that gives it a name that is different from any other object on the page. We also need to identify this `<div ...>` generally, as a carousel. So it has two attributes, `class` and `id`: 

`<div class="carousel" id="prison-bus-slideshow">`

This means that, generally, this is a carousel, and specifically I'm always going to use `prison-bus-slideshow` to refer to it in my HTML. The values you give to your `id` attribute (and any new classes you define, but that is a long ways off) are case sensitive and shouldn't include spaces or punctuation other than dashes `-` and underscores `_`. 


*[HTML]: Hyper Text Markup Lanuage
*[english]: en
*[DOM]: Document Object Model