---
layout: page
title: Blog
subtitle: Notes on Resistance, Censorship, and Code
---

<div>
{% assign postsCategory = site.posts | group_by_exp:"post", "post.categories"  %}
{% for category in postsCategory %}
{% for post in category.items %}
<h2>
<a href="{{ post.url | prepend: site.aseurl }}">
{{ post.title }}
</a>
</h2>
<span>{{ post.date | date: "%d %B %Y" }}</span>
<p>{{ post.content | strip_html | truncatewords: 50}}</p>

{% endfor %}
{% endfor %}
</div>
