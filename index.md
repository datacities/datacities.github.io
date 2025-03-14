---
layout: single
title: "Data Strategies"
author_profile: false
entries_layout: none
---
This website collects and documents data strategies from cities around the world. We also include data strategies of other entities, such as states, since these can be useful references as well. The goal of this website is to create a reference and source of inspiration for cities looking to establish or refine their data strategies.

You can contribute to this website via [GitHub](https://github.com/datacities/datacities.github.io).

## Data Strategies of Cities

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 20px;">
  {% for strategy in site.strategies %}
   {% if strategy.level == 'city' %}
    <div style="border: 1px solid #ddd; padding: 16px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      {% if strategy.thumbnail %}
        <a href="{{ site.baseurl }}{{ strategy.url }}">
          <img src="{{ strategy.thumbnail }}" alt="{{ strategy.title }} thumbnail" style="width: 100%; height: 200px; object-fit: cover; border-radius: 4px;">
        </a>
      {% endif %}
      <h3>
        <a href="{{ site.baseurl }}{{ strategy.url }}">{{ strategy.title }}</a>
      </h3>
      {% if strategy.summary %}
        <p>{{ strategy.summary | truncatewords: 20 }}</p>
      {% endif %}
    </div>
    {% endif %}
  {% endfor %}
</div>



## Data Strategies of other Entities

Here, we collect data strategies of entities that are not cities, but that we consider to be useful references.

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 20px;">
  {% for strategy in site.strategies %}
   {% unless strategy.level == 'city' %}
    <div style="border: 1px solid #ddd; padding: 16px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      {% if strategy.thumbnail %}
        <a href="{{ site.baseurl }}{{ strategy.url }}">
          <img src="{{ strategy.thumbnail }}" alt="{{ strategy.title }} thumbnail" style="width: 100%; height: 200px; object-fit: cover; border-radius: 4px;">
        </a>
      {% endif %}
      <h3>
        <a href="{{ site.baseurl }}{{ strategy.url }}">{{ strategy.title }}</a>
      </h3>
      {% if strategy.summary %}
        <p>{{ strategy.summary | truncatewords: 20 }}</p>
      {% endif %}
    </div>
    {% endunless %}
  {% endfor %}
</div>
