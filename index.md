---
layout: index
title: Jake Zimmerman
subtitle: A collection of my thoughts and writings
# The weird newlines and lack of indentation is to ensure that the Markdown list
# items aren't wrapped in paragraphs.
---

<section>

Here I write essays and pieces about what's on my mind. I also have a [tech
blog] where I discuss technical topics that I'm passionate about. If you'd like
to read more about who I am and what I've done, see [my personal site].

[tech blog]: http://blog.jez.io
[my personal site]: https://jez.io

</section>

{% comment %}
<!--
NOTE(jez): There are no collections currently. If you ever want to group a
number of essays into a collection, feel free to implement it however (note:
upon your first attempt, you settled for just doing it manually, then decided
against writing multiple essays at all.
-->

## Collections

- [On Stripe](on-stripe/)

{% endcomment %}

{% capture numposts %}{{ site.posts | size }}{% endcapture %}
{% if numposts != '0' %}
## Essays

{% for post in site.posts %}{% assign currentyear = post.date | date: "%Y" %}{% if currentyear != prevyear %}
### {{ currentyear }}
{% assign prevyear = currentyear %}{% endif %} - [{{ post.title }}]({{ site.baseurl }}{{ post.url }}), {{ post.date | date: '%B %-d' }}
{% endfor %}
{% else %}
## Essays

- *None to show.*
{% endif %}


