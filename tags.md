---
layout: page
title: Tags
excerpt: Sorted article by tags.
---

<div class="archive-tags">
  <a class="tag-item" href="#">all</a>
  {%- for tag in site.tags -%} 
    {% capture name %}{{ tag | first }}{% endcapture %}
    <a class="tag-item" href="#{{name}}">{{ name }}</a> 
  {%- endfor -%}
</div>

{%- for tag in site.tags -%}
  {%- capture name -%}{{ tag | first }}{%- endcapture -%}
  <h2 id="{{ name }}">{{ name | upcase }}</h2>
  {%- for post in site.tags[name] -%}
    <article class="post-item" id="results-container">
      <span class="post-item-date">{{ post.date | date: "%b %d, %Y" }}</span>
      <h3 class="post-item-title">
        <a href="{{ post.url }}">{{ post.title | escape }}</a>
      </h3> 
    </article>
  {%- endfor -%}
{%- endfor -%}




<section class="posts">
<h1>Tag #{{page.tag}}</h1>
    <ul>
      {% for post in site.posts %}
      {% if post.tags contains page.tag %}
      <li><a class="post" href="{{ post.url }}">{{ post.title }}</a><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time></li>
      {% endif %}
      {% endfor %}
    </ul>
	
</section>