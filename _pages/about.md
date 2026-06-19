---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

## News

- **Feb. 2026** Completed undergraduate studies in the School of Computing at KAIST.

I received my undergraduate education at the Korea Advanced Institute of Science & Technology (KAIST), where I was advised by Prof. [Hyunwoo J. Kim](https://scholar.google.com/citations?user=LfBoJt8AAAAJ&hl=en) in the [MLV Lab](https://mlv.kaist.ac.kr/).

My research interests lie in building AI agents that can automate complex, multi-step tasks, and in advancing multimodal AI systems that better understand, reason over, and interact with visual information, particularly videos.

## Education

- **Korea Advanced Institute of Science & Technology (KAIST)**, School of Computing - Undergraduate Student, Mar. 2021 - Feb. 2026

## Work Experiences

- **Smoretalk** - AI Engineer, Dec. 2024 - Aug. 2025

- **Naviworks, DX Technology Team** - Internship, AI Engineer, Feb. 2024 - Aug. 2024

- **MLV Lab, KAIST** - Undergraduate Student, advised by Prof. [Hyunwoo J. Kim](https://scholar.google.com/citations?user=LfBoJt8AAAAJ&hl=en)

## Patents

{% include patents.html %}

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
