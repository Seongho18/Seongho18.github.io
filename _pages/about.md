---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

Education
======

<table style="border: none; font-size: 1em;">
  <tr style="background: none;">
    <td style="border: none; white-space: nowrap; padding-right: 1.5em;">Feb. 2025 - Now</td>
    <td style="border: none;">Ph.D. student, School of Computing, KAIST (Advisor: Sooel Son)</td>
  </tr>
  <tr style="background: none;">
    <td style="border: none; white-space: nowrap; padding-right: 1.5em;">Feb. 2023 - Feb. 2025</td>
    <td style="border: none;">M.S., School of Computing, KAIST (Advisor: Sooel Son)</td>
  </tr>
  <tr style="background: none;">
    <td style="border: none; white-space: nowrap; padding-right: 1.5em;">Feb. 2018 - Feb. 2023</td>
    <td style="border: none;">B.S., School of Computing, KAIST</td>
  </tr>
</table>

Publications
======
{% assign publications = site.publications | sort: 'date' | reverse %}
{% for post in publications %}
<p>
<strong>{{ forloop.index }}. {{ post.title }}</strong><br>
{% assign authors_with_underline = post.authors | replace: 'Seongho Keum', '<u>Seongho Keum</u>' %}
{{ authors_with_underline }}. {% if post.top_tier %}<strong>{{ post.venue_short }}</strong>{% else %}{{ post.venue_short }}{% endif %}<br>
{% if post.paperurl %}<a href="{{ post.paperurl }}">[paper]</a> {% endif %}{% if post.bibtexurl %}<a href="{{ post.bibtexurl }}">[bib]</a> {% endif %}{% if post.codeurl %}<a href="{{ post.codeurl }}">[code]</a>{% endif %}
</p>
{% endfor %}
