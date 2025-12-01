---
layout: page
title: "Blog"
lang: en
lang_ref: blog
permalink: /en/blog/
---

Here are all the posts published with this template.

<ul>
  {% assign lang_posts = site.posts | where: "lang", page.lang %}
  {% for post in lang_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span> – {{ post.date | date: "%Y-%m-%d" }}</span>
    </li>
  {% endfor %}
</ul>
