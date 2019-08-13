---
title: Publications | Herzik Lab
layout: default
---
<div class="container">
  <div class="row">
    <div class="col-md-2">
    </div>
    <div class="col-md-8">
      <h1 class="page-title">Publications</h1>
    </div>
    <div class="col-md-2">
    </div>
  </div>
</div>


{% for publication in site.data.publications | sort: date %}

<hr style="padding-top: 1em;">
<div class="container publication">
  <div class="row">
    <div class="col-md-2">
    </div>
    <div class="col-md-8">
      {% if publication.image %}
        <img src="{{ publication.image }}" class="img-responsive"><br>
      {% endif %}
      <h4><strong><em>{{ publication.title }}</em></strong></h4><br>
      <div class="citation-spacing">{{ publication.citation }}<br>
      {% if publication.equal_contribution %}
        <div style="font-size: .8em; color: gray;">{{ publication.equal_contribution }}</div>
      {% endif %} </div>
      {% if publication.abstract %}
        <strong>Abstract</strong><br>
       <div class="abstract-text"> 
          {{ publication.abstract }}
       </div>
      {% endif %}
    </div>
    <div class="col-md-2">
    </div>
  </div>
  <div class="row" style="padding-top: 2em;">
    <div class="col-md-2">
    </div>
    <div class="col-md-4">
      <p><strong>Access the Paper</strong></p>
        <ul style="color: gray;">
          {% if publication.pmid %}
          <li>PMID: <a href="http://www.ncbi.nlm.nih.gov/pubmed/{{publication.pmid}}" alt = "pubmed link: {{publication.pmid}}"> {{publication.pmid}}</a></li>
          {% else %}
          <li>PMID: Submitted</li>
          {% endif %} 
          {% if publication.pmcid %}
          <li>PMCID: <a href="http://www.ncbi.nlm.nih.gov/pmc/articles/{{publication.pmcid}}" alt = "pubmed central link: {{publication.pmcid}}"> {{publication.pmcid}}</a></li>  
          {% else %}
          <li>PMCID: Submitted</li>
          {% endif %}
          {% if publication.biorxiv_preprint %}
          <li>Biorxiv Preprint: <a href="http://dx.doi.org/10.1101/{{publication.biorxiv}}" alt = "biorxiv preprint link: {{publication.biorxiv}}"> {{publication.biorxiv}}</a></li>
          {% endif %}
        </ul>
    </div>
    <div class="col-md-4">
      <p><strong>Additional Links</strong></p>
        <ul style="color: gray">
          {% if publication.models %}
          <li>PDBs{% if publications.models.size > 1 %}s{% endif %}:
              {% for code in publication.models %}
              <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{code}}">{{code}}</a>{% unless forloop.last %}, {% endunless %}
              {% endfor %}
          </li>
          {% endif %}
          {% if publication.maps %}
          <li>EMDBs{% if publication.maps.size > 1 %}s{% endif %}:
            {% for code in publication.maps %}
            <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/EMD-{{code}}">{{code}}</a>{% unless forloop.last %}, {% endunless %}
            {% endfor %}
          </li>
          {% endif %}
            {% if publication.raw_data %}
          <li>    Raw Data: {{ publication.raw_data }}</li>
            {% endif %}     
            {% if publication.lab %}
          <li>Lab: <a href="{{ publication.lab_link }}">{{ publication.lab }}</a></li>
            {% endif %}
            {% if publication.second_lab %}
              <li>Lab: <a href="{{ publication.second_lab_link }}">{{ publication.second_lab }}</a></li>
            {% endif %}
            {% if publication.third_lab %}
              <li>Lab: <a href="{{ publication.third_lab_link }}">{{ publication.third_lab }}</a></li>
            {% endif %}
        </ul>
    </div>
    <div class="col-md-2">
    </div>
  </div>
</div>
{% endfor %}
