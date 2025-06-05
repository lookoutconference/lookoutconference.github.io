---
layout: splash
title: Archives
permalink: /archives/
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: /assets/images/no_business_panorama.jpg
excerpt: "Explore the diverse panels and sessions from our interdisciplinary lookout conferences"
---

# Past Conferences

This page lists the sessions and links to content from past conferences. 

## NILC 2025 

<div class="notice notice--info">
<p><strong>📖 Conference Booklet:</strong> <a href="{{ site.baseurl }}/Booklet_Nilc.pdf" target="_blank">Download the full NILC 2025 Conference Booklet (PDF)</a></p>
</div>

The 2025 National Interdisciplinary Lookout Conference featured {{ site.nilc2025.size }} engaging sessions exploring various aspects of fire lookouts in the human environment. Each section brought together diverse perspectives from researchers, practitioners, and enthusiasts.

### Conference Sessions

<div class="section-grid">
{% assign sections = site.data.sections2025 %}
{% for section in sections %}
{% if section.id != 'id' %}
{% assign section_url = '/nilc2025/' | append: section.id | append: '/' %}
<div class="section-card">
<h3><a href="{{ section_url | relative_url }}">{{ section.title }}</a></h3>
{% if section.chair and section.chair != "" %}
  <p><strong>Chair:</strong> {{ section.chair }}</p>
{% endif %}

{% comment %}
<!-- List presentations and presenters in this section -->
{% endcomment %}
{% assign section_presentations = site.data.nilc2025 | where: "parentid", section.id %}
{% if section_presentations.size > 0 %}
  <div class="presentation-list">
    <p><strong>Presentations:</strong></p>
    <ul style="margin-top: 0.25rem; font-size: 0.9em;">
    {% for presentation in section_presentations %}
      <li>
        <strong>{{ presentation.speaker }}:</strong> {{ presentation.title }}
      </li>
    {% endfor %}
    </ul>
  </div>
{% endif %}

<p><a href="{{ section_url | relative_url }}" class="btn btn--primary">View Details and Videos</a></p>
</div>
{% endif %}
{% endfor %}
</div>

---

## Future Conferences

*This page will be expanded to include sections from future National Interdisciplinary Lookout Conferences as they are held.*

### Archive
- **2025**: First National Interdisciplinary Lookout Conference - University of Idaho
- **Future conferences will be listed here**