---
layout: page
title: Projects
permalink: /projects/
desc: things I've worked on.
---

<div class="page-content">

    <h2>Hardware</h2>
    {% for post in site.tags.hardware-highlight %}
      {%- include themes/{{ site.amsf_theme }}/includes/page-item-highlight.html -%}
    {% endfor %}
    
    {% for post in site.tags.hardware %}
      {%- include themes/{{ site.amsf_theme }}/includes/page-item.html -%}
    {% endfor %}

    <h2>Software</h2>
    {% for post in site.tags.software %}
      {%- include themes/{{ site.amsf_theme }}/includes/page-item.html -%}
    {% endfor %}

    <h2>Woodworking</h2>
    {% for post in site.tags.woodworking %}
      {%- include themes/{{ site.amsf_theme }}/includes/page-item.html -%}
    {% endfor %}

    <h2>Art</h2>
    {% for post in site.tags.art %}
      {%- include themes/{{ site.amsf_theme }}/includes/page-item.html -%}
    {% endfor %}

    <h2>Automotive</h2>
    {% for post in site.tags.cars %}
      {%- include themes/{{ site.amsf_theme }}/includes/page-item.html -%}
    {% endfor %}

</div>

