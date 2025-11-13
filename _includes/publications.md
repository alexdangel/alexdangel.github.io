<h2 id="publications">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<div class="pub-row">
  <div class="col-sm-9" style="position:relative;padding-right: 10px;">
      <div class="title"><b><a target="_blank" href="{{ link.pdf }}">{{ link.title }}</a></b></div>
      <div class="periodical"><b>{{ link.conference }}</b>
      <div class="author">{{ link.authors }}</div>
      </div>
    <div class="links">
      {% if link.WP %} 
      <a href="{{ link.WP }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Working Paper</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.replication %} 
      <a href="{{ link.replication}}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Replication Package</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
    <div class="col-sm-3 abbr" style="position: relative;padding-right: 10px;padding-left: 10px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
</div>

{% endfor %}

</ol>
</div>

