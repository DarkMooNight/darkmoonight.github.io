---
layout: default
title: "Store"
permalink: /store/
---
{% include slider.html %}

<h1 class="title-page">Игры</h1>

<div class="posts">
  {% for post in site.categories.store %}
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
        <p></p>
        <div class="platform">
            <img src="/images/windows-logo-silhouette.png" alt="">
            <img src="/images/linux-logo.png" alt="">
            <img src="/images/android-logo.png" alt="">
        </div>
    </div>
    </div>
    </article>
  {% endfor %}