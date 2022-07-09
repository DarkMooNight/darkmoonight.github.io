---
layout: default
title: "News"
permalink: /news/
---

<div class="s-wrap" role="slider">
  <i>
    <input checked type="radio" name="s" style="background-image: url(/images/post/comrun/Screenshot_2022-07-07-18-23-33_1920x1080.png);" title="Picture 1">
    <input type="radio" name="s" style="background-image: url(/images/post/hero-tommy/Screenshot_2022-07-08-14-41-01_1920x1080.png);" title="Picture 2">
    <input type="radio" name="s" style="background-image: url(/images/post/comrun/Screenshot_2022-07-07-18-24-34_1920x1080.png);" title="Picture 3">
    <input type="radio" name="s" style="background-image: url(/images/post/hero-tommy/Screenshot_2022-07-08-14-41-07_1920x1080.png);" title="Picture 4">
    <input type="radio" name="s" style="background-image: url(/images/post/comrun/Screenshot_2022-07-07-18-23-33_1920x1080.png);" title="Picture 5">
  </i>
</div>

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
        <p> {{ post.news }} </p>
      </div>
    </div>
  </article>
  {% endfor %}