<h2 id="publications">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<div class="pub-row">
  <div class="col-sm-9" style="position:relative;">
      <div class="title"><a target="_blank" href="{{ link.pdf }}">{{ link.title }}</a></div>
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

</div>

{% endfor %}

</ol>
</div>

