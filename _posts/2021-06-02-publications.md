---
layout: post
title: Publications
subtitle: Our scientific publications regarding TAFFO
tags: []
comments: false
last-updated: 2023-10-16

pubs:

    - title:   "Hardware and Software Support for Mixed Precision Computing: a Roadmap for Embedded and HPC Systems"
      author:  "W. Fornaciari, G. Agosta, D. Cattaneo, L. Denisov, A. Galimberti, G. Magnani, D. Zoni"
      journal: "DATE 2023"
      year:    "2023"
      url:     "https://doi.org/10.23919/DATE56975.2023.10137092"
      doi:     "https://doi.org/10.23919/DATE56975.2023.10137092"
      
    - title:   "TAFFO: The compiler-based precision tuner"
      author:  "D. Cattaneo, M. Chari, G. Agosta, S. Cherubin"
      journal: "SoftwareX"
      year:    "2022"
      url:     "https://doi.org/10.1016/j.softx.2022.101238"
      doi:     "https://doi.org/10.1016/j.softx.2022.101238"
      
    - title:   "Precision Tuning in Parallel Applications"
      author:  "G. Magnani, L. Denisov, D. Cattaneo, G. Agosta"
      journal: "PARMA-DITAM@HiPEAC 2022"
      year:    "2022"
      url:     "https://drops.dagstuhl.de/opus/volltexte/2022/16121/pdf/OASIcs-PARMA-DITAM-2022-5.pdf"
      doi:     "https://doi.org/10.4230/OASIcs.PARMA-DITAM.2022.3"
      
    - title:   "Ahead-of-Real-Time (ART): A Methodology for Static Reduction of Worst-Case Execution Time"
      author:  "D. Cattaneo, G. Magnani, S. Cherubin, G. Agosta"
      journal: "NG-RES@HiPEAC 2022"
      year:    "2022"
      url:     "https://drops.dagstuhl.de/opus/volltexte/2022/16112/pdf/OASIcs-NG-RES-2022-4.pdf"
      doi:     "https://doi.org/10.4230/OASIcs.NG-RES.2022.4"
    
    - title:   "Architecture-aware precision tuning with multiple number representation systems"
      author:  "D. Cattaneo, M. Chiari, N. Fossati, S. Cherubin, G. Agosta"
      journal: "DAC 2021"
      year:    "2021"
      url:     "https://doi.org/10.1109/DAC18074.2021.9586303"
      doi:     "https://doi.org/10.1109/DAC18074.2021.9586303"
      
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

    - title:   "Fixed point exploitation via compiler analyses and transformations: POSTER"
      author:  "D. Cattaneo, A. Di Bello, M. Chiari, S. Cherubin, G. Agosta"
      journal: "CF 2019"
      year:    "2019"
      url:     "https://doi.org/10.1145/3310273.3323424"
      doi:     "https://doi.org/10.1145/3310273.3323424"

    - title:   "Feedback-Driven Performance and Precision Tuning for Automatic Fixed Point Exploitation"
      author:  "D. Cattaneo, M. Chiari, S. Cherubin, A. Di Bello, G. Agosta"
      journal: "PARCO 2019"
      year:    "2019"
      url:     "https://doi.org/10.3233/APC200054"
      doi:     "https://doi.org/10.3233/APC200054"

    - title:   "Embedded Operating System Optimization through Floating to Fixed Point Compiler Transformation"
      author:  "D. Cattaneo, A. Di Bello, S. Cherubin, F. Terraneo, G. Agosta"
      journal: "DSD 2018"
      year:    "2018"
      url:     "https://doi.org/10.1109/DSD.2018.00042"
      doi:     "https://doi.org/10.1109/DSD.2018.00042"
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
