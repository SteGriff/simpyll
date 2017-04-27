---
---

# Hello World

Here are my posts:

<div>
{% for post in site.posts %}

	<h2>
	{{post.title}}
	</h2>

	<p>
	{{post.tags | array_to_sentence_string: 'and finally' }}
	</p>
	
	<em>
	{{post.date | date_to_long_string}}
	</em>

	{{post.content | strip_html | truncatewords : 30}}

	[Read more...]({{post.url}})
	 
{% endfor %}
</div>

<div>
{% for person in site.data.people %}
	{{person.name}}
{% endfor %}
</div>