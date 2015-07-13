---
layout: default
title: Blog
permalink: /blog/
---

<div class="home">
	<ul class="posts">
		{% for post in site.posts %}
			<li class="posts__item">
				<div class="posts__item__meta">
					<span class="posts__item__day-month">{{ post.date | date: "%-d/%b" }}</span><br>
					<span class="posts__item__year">{{ post.date | date: "%Y" }}</span>
				</div>

				<div class="posts__item__data">
					<h2>
						<a class="posts__item__link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
					</h2>

					<span class="posts__item__categories">{% for category in post.categories %} #{{category}} {% endfor %}</span>
				</div>
			</li>
		{% endfor %}
	</ul>
</div>
