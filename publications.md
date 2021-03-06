---
layout: page
title: Publications
pubs:
    - title: "A retention index-based QSPR model for the quality control of rice"
      author: "Rojas, Cristian and Tripaldi, Piercosimo and Pérez-González, Andrés and Duchowicz, Pablo R and Diez, Reinaldo Pis"
      journal: "Journal of Cereal Science"
      year: "2018"
      media:
        - name: "paper"
          url:  "https://doi.org/10.1016/j.jcs.2017.11.004"


    - title: "A novel oxidovanadium (V) compound with an isonicotinohydrazide ligand. A combined experimental and theoretical study and cytotoxity against K562 cells"
      author: "Ana C González-Baró, Verónica Ferraresi-Curotto, Reinaldo Pis-Diez, Beatriz S Parajón Costa, Jackson ALC Resende, Flávia CS de Paula, Elene C Pereira-Maia, Nicolás A Rey"
      journal: "Polyhedron"
      year: "2017"
      media:
        - name: "doi"
          url: "https://doi.org/10.1016/j.poly.2017.07.013"

    - title: "Bidimensional Spectroelectrochemistry: application of a new device in the study of a o-vanillin-copper (II) complex"
      author: "D Izquierdo, V Ferraresi-Curotto, A Heras, R Pis-Diez, AC Gonzalez-Baro, A Colina"
      journal: "Electrochimica Acta"
      year: "2017"
      media:
        - name: "doi"
          url: "https://doi.org/10.1016/j.electacta.2017.05.105"



---

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
