---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

I am an undergraduate student at the Korea Advanced Institute of Science & Technology (KAIST), working with Prof. [Hyunwoo J. Kim](https://scholar.google.com/citations?user=LfBoJt8AAAAJ&hl=en) in the [MLV Lab](https://mlv.kaist.ac.kr/). My research interests include AI agents, video understanding, and multimodal AI.

## Education

- **Korea Advanced Institute of Science & Technology (KAIST)**, School of Computing - Undergraduate Student, Mar. 2021 - Feb. 2026

## Work Experiences

- **MLV Lab, KAIST** - Undergraduate Student, advised by Prof. [Hyunwoo J. Kim](https://scholar.google.com/citations?user=LfBoJt8AAAAJ&hl=en)

## Publications

{% if site.publications.size > 0 %}
  {% if site.publication_category %}
    {% for category in site.publication_category %}
      {% assign title_shown = false %}
      {% for post in site.publications reversed %}
        {% if post.category != category[0] %}
          {% continue %}
        {% endif %}
        {% unless title_shown %}
          <h3>{{ category[1].title }}</h3>
          {% assign title_shown = true %}
        {% endunless %}
        {% include archive-single.html %}
      {% endfor %}
    {% endfor %}
  {% else %}
    {% for post in site.publications reversed %}
      {% include archive-single.html %}
    {% endfor %}
  {% endif %}
{% else %}
No publications listed yet.
{% endif %}
