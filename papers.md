---
layout: page
permalink: /papers/
title: Papers
highlight: Forer L
---

<table class="paper-table">
<thead>
<th class="left-0">Title</th>
<th class="right-0">Year</th>
</thead>
<tbody>
{% assign sorted_papers =site.papers | sort: 'number' | reverse %}
  {% for paper in sorted_papers %}
  <tr>
  <td class="left-0">
      <div class="paper-title">{% if paper.doi %}<a href="https://doi.org/{{ paper.doi }}" target="_blank">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}</div>
      <div class="paper-authors">{{paper.authors | replace: "Forer L", "<b>Forer L</b>"}}</div>
      <div class="paper-journal"><b>{{paper.journal}}</b>{% if paper.volume %} {{paper.volume}}{% if paper.issue %} ({{paper.issue}}){% endif %}{% endif %}{% if paper.pages %}, {{paper.pages}}{% endif %}. {{paper.pubdate.year}}{% if paper.pubdate.month %} {{paper.pubdate.month}}{% endif %}{% if paper.pubdate.day %}  {{paper.pubdate.day}}{% endif %}. {% if paper.pmid %}PMID: <a href="https://www.ncbi.nlm.nih.gov/pubmed/{{paper.pmid}}" target="_blank">{{paper.pmid}}</a>{% endif %}</div>
</td>
<td class="right-0">
<div class="paper-year">{{paper.pubdate.year}}</div>
</td>
</tr>
  {% endfor %}
</tbody>  
</table>
