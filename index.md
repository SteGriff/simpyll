---
---

# Hello World

Here are my posts:

{% for post in site.posts %}

## {{post.title}}

*{{post.date | date_to_string}}*

 > {{post.content | strip_html | truncatewords : 30}}
 > 
 > [Read more...]({{site.baseurl}}{{post.url}})
 
{% endfor %}