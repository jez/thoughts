---
layout: index
title: Jake Zimmerman
subtitle: A collection of my thoughts and writings
# The weird newlines and lack of indentation is to ensure that the Markdown list
# items aren't wrapped in paragraphs.
---

This site contains longer form, usually non-technical pieces of my writing. I
also have a [tech blog] where I discuss technical topics that I'm passionate
about. If you'd like to read more about who I am and what I've done, see [my
personal site].

[tech blog]: http://blog.jez.io
[my personal site]: https://jez.io

## Collections

- [On Stripe](on-stripe/)

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


