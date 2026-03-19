---
layout: default
---

# Welcome to my Portfolio

Here are some of the things I've been working on:

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
*{{ post.date | date_to_string }}* {{ post.description }}
---
{% endfor %}