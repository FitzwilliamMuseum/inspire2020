---
layout: default
permalink: /entries/
title: Inspire2020 All entries
---
<div class="container mb-3">
  <div class="row">
  {% assign rows = site.entries.size | divided_by: 2.0 | ceil %}
  {% for i in (1..rows) %}
  {% assign offset = forloop.index0 | times: 2 %}
  {% assign sorted = site.entries | sort:"title" %}
      {% for author in sorted limit:2 offset:offset %}
      <div class="col-md-4 mb-3">
        <div class="card h-100" >
          {% include structure/list-entry-image.html %}
          <div class="card-body">
            <h3 class="lead mt-2">
              <a href="{{ author.url }}" class="stretched-link">{{author.title}}</a>
            </h3>
          </div>
        </div>
      </div>
      {% endfor %}
    {% endfor %}
    </div>
</div>
