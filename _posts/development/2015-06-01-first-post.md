---
layout: page
sidebar: right
subheadline: Test post
title:  "The First Post"
teaser: "Testing if I can post new"
breadcrumb: true
tags:
    - test
categories:
    - development
image:
    thumb: "unsplash_2_thumb.jpg"
    homepage: "unsplash_2.jpg"
    title: "unsplash_2.jpg"
    caption: Unsplash.com
    caption_url: http://unsplash.com
comments: true
---
Testing if it `works` fine.

{% highlight scala %}
def fun(s: String) = "abc"
{% endhighlight %}

~~~
show_meta: true
~~~

If you don't want to show metadata, it's simple again:

~~~
show_meta: false
~~~


## Other Post Formats
{: .t60 }
{% include list-posts.html tag='test' %}
