---
layout: page
title: "Blog"
lang: fr
lang_ref: blog
permalink: /blog/
---

Voici tous les articles publiés avec ce template.

<ul>
  {% assign lang_posts = site.posts | where: "lang", page.lang %}
  {% for post in lang_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span> – {{ post.date | date: "%Y-%m-%d" }}</span>
    </li>
  {% endfor %}
</ul>
