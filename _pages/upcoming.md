---
layout: default
permalink: /upcoming/
---

## Upcoming episodes

<style>
  .post-list {
    list-style: none;
    padding: 0;
  }

  .post-item {
    background-color: #fff;
    border: 1px solid #ddd;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    margin-bottom: 15px;
    padding: 15px;
    border-radius: 8px;
  }

  .post-item h2 {
    margin-top: 0;
    color: #333;
  }

  .post-item a {
    text-decoration: none;
    color: #0066cc;
  }

  .post-item a:hover {
    text-decoration: underline;
  }

  .post-date {
    color: #777;
    font-size: 0.9em;
    margin-bottom: 10px;
    display: block;
  }

  /* Optional: if you have images */
  .post-image {
    width: 100%;
    height: auto;
    margin-bottom: 10px;
  }
</style>

<ul class="post-list">
  {% assign future_posts = site.posts | sort: "date" %}
  {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}

  {% for post in future_posts %}
    {% capture posttime %}{{ post.date | date: '%s' }}{% endcapture %}
    {% if posttime > nowunix %}
      <li class="post-item">
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <span class="post-date">{{ post.date | date: "%-d %B %Y" }}</span>
        Host(s): {{ post.hosts }}
      </li>
    {% endif %}
  {% endfor %}
</ul>
