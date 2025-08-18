---
layout: page
permalink: /categories/
title: Categories
---

<!-- Featured Categories -->
<div class="featured-categories">
  <h3>Featured Categories</h3>
  <div class="category-grid">
    <div class="category-card">
      <h4><a href="#motivation">Motivation</a></h4>
      <p>Understanding why AI safety matters and the fundamental challenges we face.</p>
    </div>
    <div class="category-card">
      <h4><a href="#policy">Policy</a></h4>
      <p>Governance frameworks, regulations, and policy recommendations for AI safety.</p>
    </div>
    <div class="category-card">
      <h4><a href="#tech">Tech</a></h4>
      <p>Technical approaches and research methods for ensuring AI safety.</p>
    </div>
    <div class="category-card">
      <h4><a href="#resources">Resources</a></h4>
      <p>Learning materials, courses, and community resources for AI safety.</p>
    </div>
  </div>


<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h4 class="category-head">{{ category_name }}</h4>
    <a name="{{ category_name | slugize }}"></a>
        <ul>
    {% for post in site.categories[category_name] %}
                <li><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></li>
        {% endfor %}
        </ul>

  </div>
{% endfor %}
</div>

</div>
