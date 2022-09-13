---
layout: default
title: Archive
---

<section class="posts">
	<h1>{{ page.title }}</h1>

<div class="archive-tags">
    <b>Tags:</b> <br>
  {%- for tag in site.tags -%} 
    {% capture name %}{{ tag | first }}{% endcapture %}
    <a class="tag-item" href="/tag/{{ tag | first | slugify }}/">{{ name }}</a> |  
  {%- endfor -%}
<br><br>
</div>



<ul>
{% for post in site.posts %}
<li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time></li>
{% endfor %}
</ul>
    

</section>

<section class="posts">



</section>


