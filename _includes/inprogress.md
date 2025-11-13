<h2 id="inprogress">In Progress</h2>

<div class="inprogress">
<ol class="bibliography">

{% for link in site.data.inprogress.main %}

<div class="pub-row">
  <div class="pub-row2">
    <div class="col-sm-9" style="position:relative;">
      <div class="title">
        <a target="_blank" href="{{ link.pdf }}" style="color:#222222">{{ link.title }}</a> 
        {% if link.authors %} 
            (with {{ link.authors }})
        {% endif %}
      </div>
      <div class="periodical">{{ link.conference }}
      </div>
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">[Published Paper]</a>
        {% endif %}
        {% if link.wp %} 
        <a href="{{ link.wp }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">[Working Paper]</a>
        {% endif %}
        {% if link.replication %} 
        <a href="{{ link.replication}}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">[Data/Code]</a>
        {% endif %}
        {% if link.abstract %} 
        <button class="toggle-abstract-btn" onclick="toggleAbstract(this)" style="font-size:12px;">[Show Abstract]</button>
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

  {% if link.abstract %} 
    <div class="abstract-container">
        <p class="abstract-text">{{ link.abstract }}</p>
    </div>
  {% endif %}
  </div>
</div>   
{% endfor %}

</ol>
</div>



