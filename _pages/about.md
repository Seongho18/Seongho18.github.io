---
permalink: /
title: "Seongho Keum"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

Publications
======
{% assign publications = site.publications | sort: 'date' | reverse %}
{% for post in publications %}
<p>
<strong>{{ forloop.index }}. {{ post.title }}</strong><br>
{{ post.authors }}. {{ post.venue_short }}<br>
{% if post.paperurl %}<a href="{{ post.paperurl }}">[paper]</a> {% endif %}{% if post.bibtexurl %}<a href="{{ post.bibtexurl }}">[bib]</a> {% endif %}{% if post.codeurl %}<a href="{{ post.codeurl }}">[code]</a>{% endif %}
</p>
{% endfor %}
