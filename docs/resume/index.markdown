---
title: Resume
permalink: /resume/
redirect_from: /r/
description: My Resume
---
<!-- This script automiticall looks through all my resume versions and displays the most recent -->
{% for i in (0..100) %}
  {% capture path %}/resume/v {{- i -}} .pdf{% endcapture %}
  {% for static_file in site.static_files %}
    {% assign stoploop = true %}
    {% if static_file.path == path %}
      {% assign actual = path %}
      {% assign stoploop = false %}
      {% break %}      
    {% endif %}
  {% endfor %}
  {% if stoploop %}
    {% break %}
  {% endif %}
{% endfor %}
{% include pdf.html url=actual %}
