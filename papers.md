---
layout: page
permalink: /papers/
highlight: Forer L
---

# Papers

<table class="paper-table">
<thead>
<th>Title</th>
<th>Year</th>
</thead>
<tbody>
{% assign sorted_papers =site.papers | sort: 'number' | reverse %}
  {% for paper in sorted_papers %}
  <tr>
  <td>
      <div class="paper-title">{% if paper.doi %}<a href="https://doi.org/{{ paper.doi }}" target="_blank">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}</div>
      <div class="paper-authors">{{paper.authors | replace: "Forer L", "<b>Forer L</b>"}}</div>
      <div class="paper-journal"><b>{{paper.journal}}</b>{% if paper.volume %} {{paper.volume}}{% if paper.issue %} ({{paper.issue}}){% endif %}{% endif %}{% if paper.pages %}, {{paper.pages}}{% endif %}. {{paper.pubdate.year}}{% if paper.pubdate.month %} {{paper.pubdate.month}}{% endif %}{% if paper.pubdate.day %}  {{paper.pubdate.day}}{% endif %}. {% if paper.pmid %}PMID: <a href="https://www.ncbi.nlm.nih.gov/pubmed/{{paper.pmid}}" target="_blank">{{paper.pmid}}</a>{% endif %}</div>
</td>
<td>
<div class="paper-year">{{paper.pubdate.year}}</div>
</td>
</tr>
  {% endfor %}
</tbody>  
</table>
