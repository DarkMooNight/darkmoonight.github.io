---
layout: default
title: "News"
permalink: /news/
---
{% include slider.html %}

<h1 class="title-page">Новости</h1>

<div class="posts">
  {% for post in site.categories.news %}
    <article class="post">
    <div class="blog-card">
    <div class="meta">
      <div class="photo" style="background-image: url( {{ post.images }} )"></div>
      <ul class="details">
        <li class="author">{{ post.author }}</li>
        <li class="date">{{ post.date | date: "%B %e, %Y" }}</li>
      </ul>
    </div>
    <div class="description">
      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>
      <h2>{{ post.descriproin }}</h2>
      <p> {{ post.excerpt }} </p>
    </div>
    </div>
    </article>
  {% endfor %}