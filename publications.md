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


{% for publication in site.data.publications %}

<hr style="padding-top: 1em;">
<div class="container publication">
  <div class="row">
    <div class="col-md-2">
    </div>
    <div class="col-md-8">
      {% if publication.image %}
        <img src="{{ publication.image }}" class="img-responsive"><br>
      {% endif %}
      <h4><strong>{{ publication.title }}</strong></h4><br>
      <div class="citation-spacing">{{ publication.citation }}<br>
      {% if publication.equal_contribution %}
        <div style="font-size: .8em; color: gray;">{{ publication.equal_contribution }}</div>
      {% endif %} </div>
      {% if publication.abstract %}
        <strong>Abstract</strong><br>
        {{ publication.abstract }}
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
          <li>PMID: {{ publication.pmid }}</li>
          <li>PMCID: {{ publication.pmcid }}</li>  
            {% if publication.biorxiv_preprint %}
          <li>    Biorxiv Preprint: <a href="{{ publication.biorxiv_link }}">{{ publication.biorxiv_preprint }}</a></li>
            {% endif %}
        </ul>
    </div>
    <div class="col-md-4">
      <p><strong>Additional Links</strong></p>
        <ul style="color: gray">
          <li>PDBs: {{ publication.pdb }} </li>
          <li>EMDBs: {{ publication.emdb }} </li>
            {% if publication.raw_data %}
          <li>    Raw Data: {{ publication.raw_data }}</li>
            {% endif %}     
            {% if publication.lab %}
          <li>Lab: <a href="{{ publication.lab_link }}">{{ publication.lab }}</a></li>
            {% endif %}
        </ul>
    </div>
    <div class="col-md-2">
    </div>
  </div>
</div>
{% endfor %}
