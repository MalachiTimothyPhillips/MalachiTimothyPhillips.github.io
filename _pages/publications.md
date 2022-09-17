---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

These are a few highlights from some recent papers.
A biblatex file including all of my publications may be accessed here:
[references.bib](https://MalachiTimothyPhillips.github.io/files/references.bib)

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
