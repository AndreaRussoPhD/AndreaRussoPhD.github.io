---
permalink: /
title: "Andrea Russo"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am currently a Postdoctoral Researcher in Computational Social Science at the University of Pavia, working on the [AlgoFeed project](https://algofeed.unimi.it/), and collaborating with [Prof. Alessandro Caliandro](https://www.unimi.it/it/ugov/person/alessandro-caliandro) at the Department of Social and Political Sciences at The University of Milan, Milan, Ialy. My research interests are broadly in the intersection of Social media, network science, AI/LLMs, data analytics, security, and politics.



## Research Interest
- Computational Social Science, Sociology, Marketing, Security Studies, and Political Studies.
- Complex Systems, Collective Intelligence, Self-Organized Criticality, and Stochastic Resonance.
- Artificial Intelligence, Space Industry, Natural Language Processing (NLP), and Network Science.



## News

<ul>
{% for item in site.data.news %}
  <li><strong>{{ item.date }}.</strong>
    {% if item.link and item.link != "" %}
      <a href="{{ item.link }}">{{ item.text }}</a>
    {% else %}
      {{ item.text }}
    {% endif %}
  </li>
{% endfor %}
</ul>

## Featured Publications

{% for pub in site.data.featured_publications %}

{% if pub.image %}
<img src="{{ pub.image | relative_url }}"
     style="max-width:200px; float:left; margin-right:15px;">
{% endif %}

**{{ pub.title }}**  
{{ pub.authors }}  
*{{ pub.venue }}*, {{ pub.year }}  

{% if pub.paperurl %}
[PDF]({{ pub.paperurl }})
{% endif %}

<div style="clear:both;"></div>

{% endfor %}
