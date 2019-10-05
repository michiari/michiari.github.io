---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "Word- and Tree-based Temporal Logics for Operator Precedence Languages"
      author:  "M. Chiari, D. Mandrioli, M. Pradella"
      journal: "ICTCS"
      year:    "2019"
      doi:     "http://dx.doi.org"

    - title:   "Temporal Logic and Model Checking for Operator Precedence Languages"
      author:  "M. Chiari, D. Mandrioli, M. Pradella"
      journal: "GandALF"
      year:    "2018"
      url:     "http://eptcs.web.cse.unsw.edu.au/paper.cgi?GandALF18.12"
      doi:     "http://dx.doi.org/10.4204/EPTCS.277.12"

---

## Publications (peer reviewed)

Disclaimer: this list of publications might be outdated.
For a more updated one, here's my [DBLP](https://dblp1.uni-trier.de/pers/hd/c/Chiari:Michele).

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
