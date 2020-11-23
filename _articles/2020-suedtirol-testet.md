---
layout: article
date: 22. November 2020, 20:00 Uhr
title: Südtirol testet
---

Vom 20. November 2020 bis zum 22. November 2020 wurde in Südtirol ein dreitägiger kostenloser Massentest durchgeführt, um mit Hilfe von Antigen-Tests die gesamte Bevölkerung flächendeckend auf COVID19 Infektion zu untersuchen. [Weitere Informationen](https://coronatest.sabes.it/de).

Die Test-Ergebnisse wurden fortlaufend auf den Seiten des [Südtiroler Sanitätsbetriebs
](https://coronatest.sabes.it/de/muni) veröffentlicht. Diese Daten dienten als Grundlage, um die Beteiligung der Bevölkerung im Zeitraffer darzustellen.

<div style="margin-top: 50px; margin-bottom: 50px;">
<img src="/images/2020-suedtirol-testet/animation-01.gif">
</div>

Die Visualisierung wurde mit der freien Software [R](https://www.r-project.org) und den Paketen [ggplot2](https://ggplot2.tidyverse.org) und [gganimate](https://gganimate.com) erstellt:

- Für eine flüssige Animation wurden immer 2-Stunden-Intervalle verwendet. Die fehlenden Intervalle wurden interpoliert.
- Die geographischen Daten der Gemeinden stammen von [https://geoservices.buergernetz.bz.it/geokatalog](https://geoservices.buergernetz.bz.it/geokatalog).
- Die Test-Ergebnisse stammen von [https://coronatest.sabes.it/de/muni](https://coronatest.sabes.it/de/muni).
