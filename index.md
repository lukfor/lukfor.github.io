---
layout: default
---

<h1>About</h1>

Hello, I'm Lukas Forer, a researcher and software developer living in Innsbruck, Austria. My main interests are Bioinformatics, Cloud Computing and Big Data. I love building [scientific applications](http://www.forer.it/projects) that are efficient and beautiful. This page shows you some of my ongoing projects. For more information about my scientific publications, please read my [CV](http://lukfor.github.io/files/CV_and_Publications_Forer.pdf) or visit my [Google Scholar profile](http://scholar.google.at/citations?user=9m0ch2QAAAAJ&hl=de).

<h2>Blog Posts</h2>

<div class="posts">
  <ul>
  {% for post in site.posts %}     
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
</div>
