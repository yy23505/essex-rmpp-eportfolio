---
layout: splash
title: Research Methods & Professional Practice
subtitle: MSc Computer Science — University of Essex Online
header:
  overlay_color: "#000"
  overlay_filter: "0.35"
  overlay_image: {{ site.baseurl }}/assets/headers/hero.jpg
excerpt: >
  This e-portfolio evidences learning across research ethics, literature reviewing,
  inferential statistics, and proposal design. Explore the units below.
---

{% assign unit_cards = site.units | sort: 'title' %}
{% capture features %}
{% for u in unit_cards %}
- image_path: {{ site.baseurl }}/assets/headers/unit.jpg
  alt: "{{ u.title }}"
  title: "{{ u.title }}"
  excerpt: "{{ u.summary | default: 'View page' }}"
  url: "{{ site.baseurl }}{{ u.url }}"
  btn_label: "Open"
  btn_class: "btn--primary"
{% endfor %}
{% endcapture %}
{% assign features_list = features | split: '\n\n' %}
{% include feature_row %}
