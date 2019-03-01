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
        {{ publiaction.image }}
      {% endif %}
      <h4><strong>{{ publication.title }}</strong></h4><br>
      {{ publication.citation }}<br>
      {% if publication.equal_contribution %}
        <p style="font-size: .8em; color: gray;">{{ publication.equal_contribution }}</p>
      {% endif %}
    </div>
    <div class="col-md-2">
    </div>
  </div>
  <div class="row" style="padding-top: 1em;">
    <div class="col-md-2">
    </div>
    <div class="col-md-4">
      <p><strong>Access the Paper</strong></p>
        <ul style="color: gray;">
          <li>PMID: {{ publication.pmid }}</li>
          <li>PMCID: {{ publication.pmcid }}</li>
          <li>
            {% if publication.biorxiv_preprint %}
              Biorxiv Preprint: <a href="{{ publication.biorxiv_link }}">{{ publication.biorxiv_preprint }}</a>
            {% endif %}
          </li>
        </ul>
    </div>
    <div class="col-md-4">
      <p><strong>Additional Links</strong></p>
        <ul style="color: gray">
          <li>PDBs: {{ publication.pdb }} </li>
          <li>EMDBs: {{ publication.emdb }} </li>
          <li>
            {% if publication.raw_data %}
              Raw Data: {{ publication.raw_data }}
            {% endif %}
           </li>
          <li>
            {% if publication.lab %}
              Lab: <a href="{{ publication.lab_link }}">{{ publication.lab }}</a>
            {% endif %}
          </li>
        </ul>
    </div>
    <div class="col-md-2">
    </div>
  </div>
</div>
{% endfor %}
