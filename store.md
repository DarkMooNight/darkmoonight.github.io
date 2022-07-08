---
layout: default
title: "Store"
permalink: /store/
---

<div class="s-wrap s-type-1" role="slider">
  <input type="radio" id="s-1" name="slider-control" checked="checked">
  <input type="radio" id="s-2" name="slider-control">
  <input type="radio" id="s-3" name="slider-control">
  <input type="radio" id="s-4" name="slider-control">
  <input type="radio" id="s-5" name="slider-control">
  <ul class="s-content">
    <li class="s-item s-item-1"><img src="/images/post/hero-tommy/Screenshot_2022-07-08-14-41-01_1920x1080.png" alt=""></li>
    <li class="s-item s-item-1"><img src="/images/post/hero-tommy/Screenshot_2022-07-08-14-41-17_1920x1080.png" alt=""></li>
    <li class="s-item s-item-1"><img src="/images/post/comrun/Screenshot_2022-07-07-18-23-33_1920x1080.png" alt=""></li>
    <li class="s-item s-item-1"><img src="/images/post/comrun/Screenshot_2022-07-07-18-24-48_1920x1080.png" alt=""></li>
    <li class="s-item s-item-1"><img src="/images/post/comrun/Screenshot_2022-07-07-18-25-23_1920x1080.png" alt=""></li>
  </ul>
  <div class="s-control">
    <label class="s-c-1" for="s-1"></label>
    <label class="s-c-2" for="s-2"></label>
    <label class="s-c-3" for="s-3"></label>
    <label class="s-c-4" for="s-4"></label>
    <label class="s-c-5" for="s-5"></label>
  </div>
  <div class="s-nav">
    <label class="s-nav-1 right" for="s-2"></label>
    <label class="s-nav-2 left" for="s-1"></label>
    <label class="s-nav-2 right" for="s-3"></label>
    <label class="s-nav-3 left" for="s-2"></label>
    <label class="s-nav-3 right" for="s-4"></label>
    <label class="s-nav-4 left" for="s-3"></label>
    <label class="s-nav-4 right" for="s-5"></label>
    <label class="s-nav-5 left" for="s-4"></label>
  </div>
</div>

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
          <img src="/images/os/windows-logo-silhouette.png" alt="">
          <img src="/images/os/linux-logo.png" alt="">
          <img src="/images/os/android-logo.png" alt="">
        </div>
      </div>
    </div>
  </article>
  {% endfor %}