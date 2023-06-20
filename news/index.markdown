---
layout: default
title: MWorks News
---

## MWorks News ##

To stay up to date with MWorks news, subscribe to our <a href="/atom.xml">RSS feed</a> or join our <a href="http://mailman.mit.edu/mailman/listinfo/mworks-users">mailing list</a>.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date_to_string }})
    </li>
  {% endfor %}
</ul>
