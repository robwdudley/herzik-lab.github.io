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
            <div class="paper-title">
                <h4><strong><em>{{ publication.title }}</em></strong></h4><br>
            </div>
            <div class="journal-title">
                <em>{{ publication.journal }}</em>
                    {{ publication.date }}
            </div>
            <div class="citation-spacing">{{ publication.authors }}<br>
                {% if publication.equal_contribution %}
                    <div style="font-size: .8em; color: gray;">
                        {{ publication.equal_contribution }}
                    </div>
                {% endif %} 
            </div>
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
                      <li>Biorxiv Preprint: <a href="http://dx.doi.org/10.1101/{{publication.biorxiv_preprint}}" alt = "biorxiv preprint link: {{publication.biorxiv_preprint}}"> {{publication.biorxiv_preprint}}</a></li>
                    {% endif %}
                </ul>
        </div>
        <div class="col-md-4">
            <p><strong>Additional Links</strong></p>
                <ul style="color: gray">
                    {% if publication.pdb1 %}
                        <li>PDB: <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb1}}"{{pdb1}}</a></li>
                    {% else %}
                    {% if publication.pdb2 %}
                        <li>PDBs: <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb1}}"{{pdb1}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb2}}"{{pdb2}}</a></li>
                    {% else %}
                    {% if publication.pdb3 %}
                        <li>PDBs: <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb1}}"{{pdb1}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb2}}"{{pdb2}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb3}}"{{pdb3}}</a></li>
                    {% else %}
                    {% if publication.pdb4 %}
                        <li>PDBs: <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb1}}"{{pdb1}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb2}}"{{pdb2}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb3}}"{{pdb3}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb4}}"{{pdb4}}</a></li>
                    {% else %}
                    {% if publication.pdb5 %}
                        <li>PDBs: <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb1}}"{{pdb1}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb2}}"{{pdb2}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb3}}"{{pdb3}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb4}}"{{pdb4}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb5}}"{{pdb5}}</a></li>
                    {% else %}
                    {% if publication.pdb6 %}
                        <li>PDBs: <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb1}}"{{pdb1}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb2}}"{{pdb2}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb3}}"{{pdb3}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb4}}"{{pdb4}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb5}}"{{pdb5}}</a>, <a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{pdb1}}"{{pdb1}}</a></li>
                    {% endif %}
                    {% if publication.emdb1 %}
                        <li>EMDB: <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb1}}">{{emdb1}}</a></li>
                    {% else %}
                    {% if publication.emdb2 %}
                        <li>EMDB: <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb1}}">{{emdb1}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb2}}">{{emdb2}}</a></li>
                    {% else %}
                    {% if publication.emdb3 %}
                        <li>EMDB: <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb1}}">{{emdb1}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb2}}">{{emdb2}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb3}}">{{emdb3}}</a></li>
                    {% else %}
                    {% if publication.emdb4 %}
                        <li>EMDB: <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb1}}">{{emdb1}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb2}}">{{emdb2}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb3}}">{{emdb3}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb4}}">{{emdb4}}</a></li>
                    {% else %}
                    {% if publication.emdb5 %}
                        <li>EMDB: <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb1}}">{{emdb1}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb2}}">{{emdb2}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb3}}">{{emdb3}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb4}}">{{emdb4}}</a>, <a href="http://www.ebi.ac.uk/pdbe/entry/emdb/{{emdb5}}">{{emdb5}}</a></li>
                    {% endif %}
                    {% if publication.raw_data1 %}
                        <li>Raw Data: <a https://www.ebi.ac.uk/pdbe/emdb/empiar/entry/{{publication.raw_data1}}">{{publication.raw_data1}}</a></li>
                    {% else %}  
                    {% if publication.raw_data2 %}
                        <li>Raw Data: <a https://www.ebi.ac.uk/pdbe/emdb/empiar/entry/{{publication.raw_data1}}">{{publication.raw_data1}}</a>, <a https://www.ebi.ac.uk/pdbe/emdb/empiar/entry/{{publication.raw_data2}}">{{publication.raw_data2}}</a></li>
                    {% else %}
                    {% if publication.raw_data3 %}
                        <li>Raw Data: <a https://www.ebi.ac.uk/pdbe/emdb/empiar/entry/{{publication.raw_data1}}">{{publication.raw_data1}}</a>, <a https://www.ebi.ac.uk/pdbe/emdb/empiar/entry/{{publication.raw_data2}}">{{publication.raw_data2}}</a>, <a https://www.ebi.ac.uk/pdbe/emdb/empiar/entry/{{publication.raw_data3}}">{{publication.raw_data3}}</a></li>
                    {% else %}
                    {% endif %}
                    {% if publication.lab %}
                        <li><a href="{{ publication.lab_link }}">{{ publication.lab }}</a></li>
                    {% endif %}
                    {% if publication.second_lab %}
                        <li><a href="{{ publication.second_lab_link }}">{{ publication.second_lab }}</a></li>
                    {% endif %}
                    {% if publication.third_lab %}
                        <li><a href="{{ publication.third_lab_link }}">{{ publication.third_lab }}</a></li>
                    {% endif %}
                </ul>
        </div>
        <div class="col-md-2">
        </div>
  </div>
</div>

{% endfor %}
