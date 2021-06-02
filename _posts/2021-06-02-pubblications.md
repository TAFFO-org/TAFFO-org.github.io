---
layout: post
title: Pubblications
subtitle: Our scientific pubblications regarding TAFFO
tags: []
comments: false
last-updated: 2021-06-02

pubs:

    - title:   "FixM: Code generation of fixed point mathematical functions"
      author:  "D. Cattaneo, M. Chiari, G. Magnani, N. Fossati, S. Cherubin, G. Agosta"
      journal: "Sustain. Comput. Informatics Syst. 29"
      year:    "2021"
      url:     "https://doi.org/10.1016/j.suscom.2020.100478"
      doi:     "https://doi.org/10.1016/j.suscom.2020.100478"

    - title:   "The Impact of Precision Tuning on Embedded Systems Performance: A Case Study on Field-Oriented Control"
      author:  "G. Magnani, D. Cattaneo, M. Chiari, G. Agosta"
      journal: "PARMA-DITAM@HiPEAC 2021"
      year:    "2021"
      url:     "https://doi.org/10.4230/OASIcs.PARMA-DITAM.2021.3"
      doi:     "https://doi.org/10.4230/OASIcs.PARMA-DITAM.2021.3"

    - title:   "Dynamic Precision Autotuning with TAFFO"
      author:  "S. Cherubin, D. Cattaneo, M. Chiari, G. Agosta"
      journal: "ACM Trans. Archit. Code Optim. 17(2)"
      year:    "2020"
      url:     "https://doi.org/10.1145/3388785"
      doi:     "https://doi.org/10.1145/3388785"

    - title:   "Automated Precision Tuning in Activity Classification Systems: A Case Study"
      author:  "N. Fossati, D. Cattaneo, M. Chiari, S. Cherubin, G. Agosta"
      journal: "PARMA-DITAM@HiPEAC 2020"
      year:    "2020"
      url:     "https://doi.org/10.1145/3381427.3381432"
      doi:     "https://doi.org/10.1145/3381427.3381432"

    - title:   "TAFFO: Tuning Assistant for Floating to Fixed Point Optimization"
      author:  "S. Cherubin, D. Cattaneo, M. Chiari, A. Di Bello, G. Agosta"
      journal: "IEEE Embed. Syst. Lett. 12(1)"
      year:    "2020"
      url:     "https://doi.org/10.1109/LES.2019.2913774"
      doi:     "https://doi.org/10.1109/LES.2019.2913774"
---

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %}){:target="_blank"}<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *({{pub.year}})* {% if pub.doi %}[[doi]({{pub.doi}}){:target="_blank"}]{% endif %}
{% if pub.prepr %}[[preprint]({{pub.prepr}}){:target="_blank"}]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}
{% endfor %}
