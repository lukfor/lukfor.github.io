---
layout: page
permalink: /papers/
title: Papers
highlight: Forer L
---

Visit me on [Google Scholar](https://scholar.google.at/citations?hl=en&user=9m0ch2QAAAAJ).

{% assign group_papers_by_year = site.papers  | group_by: 'pubdate.year' | reverse %}
{% for year in group_papers_by_year %}
<h2>{{year.name}}</h2>
<table class="paper-table">
<thead>
<th></th>
</thead>
<tbody>
  {% assign papers_sorted =  year.items  | sort  'number' | reverse %}
  {% for paper in papers_sorted %}
  <tr>
  <td class="left-0">
      <div class="paper-title">{% if paper.doi %}<a href="https://doi.org/{{ paper.doi }}" target="_blank">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}</div>
      <div class="paper-authors">{{paper.authors | replace: "Forer L", "<b>Forer L</b>"}}</div>
      <div class="paper-journal"><b>{{paper.journal}}</b>{% if paper.volume %} {{paper.volume}}{% if paper.issue %} ({{paper.issue}}){% endif %}{% endif %}{% if paper.pages %}, {{paper.pages}}{% endif %}. {{paper.pubdate.year}}{% if paper.pubdate.month %} {{paper.pubdate.month}}{% endif %}{% if paper.pubdate.day %}  {{paper.pubdate.day}}{% endif %}. {% if paper.pmid %}PMID: <a href="https://www.ncbi.nlm.nih.gov/pubmed/{{paper.pmid}}" target="_blank">{{paper.pmid}}</a>{% endif %}</div>
</td>

</tr>
  {% endfor %}
  </tbody>  
  </table>
  {% endfor %}  
