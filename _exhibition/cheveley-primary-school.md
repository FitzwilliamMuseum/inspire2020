---
title: Entries from Cheveley Primary School
layout: default
school: cheveley
image: /images/entries/zeus.jpeg
---
<div class="container mb-3">
  <div class="row">
  {% for post in site.entries %}
    {% if post.school contains page.school %}
    <div class="col-md-4 mb-3">
      <div class="card h-100" >
        <a href="{{ post.url }}" class="stretched-link">
        {% include structure/entry-image.html %}
        </a>
        <div class="card-body">
          <h3 class="lead mt-2">
            <a href="{{ post.url }}" class="stretched-link">{{post.title}}</a>
          </h3>
        </div>
      </div>
    </div>
    {% endif %}
  {% endfor %}
  </div>
</div>
