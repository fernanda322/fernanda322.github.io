---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<div class="profile" markdown="1">
  <div class="profile-photo">
    <img class="avatar" src="assets/images/foto_square1.jpg" alt="Fernanda Ramadhan Putra Hartono" />  
  </div>
  <div class="description" markdown="1">
# Halo, saya Fernanda Ramadhan.
## Bukan seorang programmer ataupun seorang IT Profesional, tapi suka belajar, berkarya dan membuat sesuatu dengan pemrograman. Halaman ini adalah ruang bagi saya untuk berekspresi.
  </div>
</div>
<hr>


<div class="content">
<div class="blog-list" markdown="1">

## Blog

  <ul>
    {% for post in site.posts %}
      {% if post.category == 'blog' %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date_to_long_string }}
      </li>
      {% endif %}
    {% endfor %}
  </ul>

## Beberapa Project yang pernah saya kerjakan ...
  <ul>
      {% for post in site.posts %}
        {% if post.category == 'project' %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date_to_long_string }}
        </li>
        {% endif %}
      {% endfor %}
    </ul>
</div>

<div class="sidebar" markdown="1">
## Sajak
  <ul>
    {% for post in site.posts %}
      {% if post.category == 'sajak' %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
      {% endif %}
    {% endfor %}
  </ul>
## Singkat Cerita
  <ul>
    {% for post in site.posts %}
      {% if post.category == 'katamotivasi' %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> 
      </li>
      {% endif %}
    {% endfor %}
  </ul>

</div>
</div>
