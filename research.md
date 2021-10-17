---
layout: page
permalink: /research/
title: Research
opl:

    - title:   "Model-Checking Structured Context-Free Languages"
      author:  "M. Chiari, D. Mandrioli, M. Pradella"
      journal: "CAV 2021, LNCS 12760: 387--410"
      year:    "2021"
      url:     "https://ucl-pplv.github.io/CAV21/poster_P_66/"
      doi:     "https://doi.org/10.1007/978-3-030-81688-9_18"
      prepr:   "/papers/CAV21.pdf"
      media:   "https://youtu.be/KTV05m_TnD4"

    - title:   "Operator Precedence Temporal Logic and Model Checking"
      author:  "M. Chiari, D. Mandrioli, M. Pradella"
      journal: "Theor. Comput. Sci. 848: 47--81"
      year:    "2020"
      url:     "https://doi.org/10.1016/j.tcs.2020.08.034"
      doi:     "https://doi.org/10.1016/j.tcs.2020.08.034"
      prepr:   "/papers/TCS20.pdf"

    - title:   "Linear Temporal Logics for Structured Context-Free Languages"
      author:  "M. Chiari, D. Bergamaschi, D. Mandrioli, M. Pradella"
      journal: "ICTCS 2020, CEUR Workshop Proceedings 2756: 115--121"
      year:    "2020"
      url:     "http://ceur-ws.org/Vol-2756/paper\_11.pdf"

    - title:   "Word- and Tree-based Temporal Logics for Operator Precedence Languages"
      author:  "M. Chiari, D. Mandrioli, M. Pradella"
      journal: "ICTCS 2019, CEUR Workshop Proceedings 2504: 222--228"
      year:    "2019"
      url:     "http://ceur-ws.org/Vol-2504/paper25.pdf"

    - title:   "Temporal Logic and Model Checking for Operator Precedence Languages"
      author:  "M. Chiari, D. Mandrioli, M. Pradella"
      journal: "GandALF 2018, EPTCS 277: 161--175"
      year:    "2018"
      url:     "http://eptcs.web.cse.unsw.edu.au/paper.cgi?GandALF18.12"
      doi:     "http://dx.doi.org/10.4204/EPTCS.277.12"

taffo:

    - title:   "FixM: Code generation of fixed point mathematical functions"
      author:  "D. Cattaneo, M. Chiari, G. Magnani, N. Fossati, S. Cherubin, G. Agosta"
      journal: "Sustain. Comput. Informatics Syst. 29 Part B: 100478"
      year:    "2021"
      url:     "https://doi.org/10.1016/j.suscom.2020.100478"
      doi:     "https://doi.org/10.1016/j.suscom.2020.100478"

    - title:   "The Impact of Precision Tuning on Embedded Systems Performance: A Case Study on Field-Oriented Control"
      author:  "G. Magnani, D. Cattaneo, M. Chiari, G. Agosta"
      journal: "PARMA-DITAM@HiPEAC 2021, OASIcs 88: 3:1--3:13"
      year:    "2021"
      url:     "https://doi.org/10.4230/OASIcs.PARMA-DITAM.2021.3"
      doi:     "https://doi.org/10.4230/OASIcs.PARMA-DITAM.2021.3"

    - title:   "Dynamic Precision Autotuning with TAFFO"
      author:  "S. Cherubin, D. Cattaneo, M. Chiari, G. Agosta"
      journal: "ACM Trans. Archit. Code Optim. 17(2): 10:1--10:26"
      year:    "2020"
      url:     "https://doi.org/10.1145/3388785"
      doi:     "https://doi.org/10.1145/3388785"

    - title:   "Automated Precision Tuning in Activity Classification Systems: A Case Study"
      author:  "N. Fossati, D. Cattaneo, M. Chiari, S. Cherubin, G. Agosta"
      journal: "PARMA-DITAM@HiPEAC 2020: 5:1--5:6"
      year:    "2020"
      url:     "https://doi.org/10.1145/3381427.3381432"
      doi:     "https://doi.org/10.1145/3381427.3381432"

    - title:   "TAFFO: Tuning Assistant for Floating to Fixed Point Optimization"
      author:  "S. Cherubin, D. Cattaneo, M. Chiari, A. Di Bello, G. Agosta"
      journal: "IEEE Embed. Syst. Lett. 12(1): 5--8"
      year:    "2020"
      url:     "https://doi.org/10.1109/LES.2019.2913774"
      doi:     "https://doi.org/10.1109/LES.2019.2913774"

eclair:

    - title:   "A Practical Approach to Verification of Floating-Point C/C++ Programs with math.h/cmath Functions"
      author:  "R. Bagnara, M. Chiari, R. Gori, A. Bagnara"
      journal: "ACM Trans. Softw. Eng. Methodol. 30(1): 9:1--9:53"
      year:    "2021"
      note:    "Presented at ICSE 2021 Journal-First"
      url:     "https://doi.org/10.1145/3410875"
      doi:     "https://doi.org/10.1145/3410875"
      prepr:   "https://arxiv.org/abs/1610.07390"
      media:   "https://youtu.be/T9zq7qG-B-c"

---

If you like little squares, here's my [DBLP](https://dblp1.uni-trier.de/pers/hd/c/Chiari:Michele){:target="_blank"}.

{% assign thumbnail="left" %}


## Context-Free Temporal Logic

{% for pub in page.opl %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %}){:target="_blank"}<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *({{pub.year}})* {% if pub.doi %}[[doi]({{pub.doi}}){:target="_blank"}]{% endif %}
{% if pub.prepr %}[[preprint]({{pub.prepr}}){:target="_blank"}]{% endif %}
{% if pub.media %}[[video]({{pub.media}}){:target="_blank"}]{% endif %}
{% endfor %}


## Floating-Point Program Verification

{% for pub in page.eclair %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %}){:target="_blank"}<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *({{pub.year}})* {% if pub.doi %}[[doi]({{pub.doi}}){:target="_blank"}]{% endif %}
{% if pub.prepr %}[[preprint]({{pub.prepr}}){:target="_blank"}]{% endif %}
{% if pub.media %}[[video]({{pub.media}}){:target="_blank"}]{% endif %}
{% endfor %}


## Approximate Computing

{% for pub in page.taffo %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %}){:target="_blank"}<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *({{pub.year}})* {% if pub.doi %}[[doi]({{pub.doi}}){:target="_blank"}]{% endif %}
{% if pub.prepr %}[[preprint]({{pub.prepr}}){:target="_blank"}]{% endif %}
{% if pub.media %}[[video]({{pub.media}}){:target="_blank"}]{% endif %}
{% endfor %}
