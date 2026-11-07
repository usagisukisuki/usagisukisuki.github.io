---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Experience
======
* **Research Engineer**, [K2I Ltd.](https://k2i.jp/) (Feb 2025 – Present)
* **Research Engineer**, SenseTime Japan Ltd. (Apr 2024 – Jan 2025)
* **JSPS Research Fellowship (DC2)** (Apr 2023 – Mar 2024)
* **Special Assistant**, Faculty of Science and Engineering, Meijo University (Apr 2021 – Mar 2023)

Education
======
* **Ph.D. (Doctor of Engineering)**, Graduate School of Science and Engineering, Meijo University (Apr 2021 – Mar 2024)
* **M.Eng. (Master of Engineering)**, Graduate School of Science and Engineering, Meijo University (Apr 2019 – Mar 2021)
* **B.Eng. (Bachelor of Engineering)**, Faculty of Engineering, Meijo University (Apr 2015 – Mar 2019)

Research Interests
======
* Computer vision and pattern recognition
* Edge and mobile AI (real-time models for low-TOPS hardware)
* Adaptation of foundation and large-scale models
* Learning under class imbalance
* Medical and biological image analysis

Awards and Grants
======
See [Achievements]({{ base_path }}/achievements/).

Publications
======
{% for category in site.publication_category %}
  {% assign posts_in_category = site.publications | where: "category", category[0] %}
  {% if posts_in_category.size > 0 %}
<h2>{{ category[1].title }}</h2>
<ul>{% for post in posts_in_category reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
  {% endif %}
{% endfor %}
