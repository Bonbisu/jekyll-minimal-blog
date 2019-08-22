---
layout: default
title: Blog
permalink: /blog
---

{% if site.posts.size == 0 %}
{% include nav.html %}

<h2>No posts found =(</h2>
{% else %}
<div class="container-blog">
{% include nav.html %}

</div>

---

{% for post in site.posts %}

<div class="content-list">
    <div class="list-item">
        <h2 class="list-post-title">
            <a href="{{ post.url | prepend: site.baseurl }}">{{
                post.title
            }}</a>
        </h2>
        <div class="list-post-date">
            <time>{{ post.date | date_to_string }}</time>
        </div>
    </div>
</div>
{% endfor %}{% endif %}
