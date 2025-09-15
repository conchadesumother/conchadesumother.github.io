---
layout: page
title: Portafolio
permalink: /portafolio/
---

¡Bienvenidos a mi portafolio! Aquí encontrarás una selección de mis trabajos y proyectos. Haz clic en las imágenes para ver los detalles de cada uno.

<br>
<hr>
<br>

<div class="posts">
  {% for post in site.posts %}
    {% if post.category == 'portafolio' %}
      <article class="post">
        <div class="post-image-container">
          <img src="{{ site.baseurl }}{{ post.image }}" alt="{{ post.title }}" class="post-image">
        </div>
        <div class="post-content">
          <a href="{{ site.baseurl }}{{ post.url }}" class="post-link">
            <h2 class="post-title">{{ post.title }}</h2>
          </a>
          <p class="post-excerpt">{{ post.excerpt }}</p>
        </div>
      </article>
    {% endif %}
  {% endfor %}
</div>
