<h2 id="Working Paper" style="margin: 2px 0px -15px;">Working Paper</h2>
<div class="publications">
<ol class="bibliography">
{% for link in site.data.publications.main %}
<li>
<div class="pub-row">
  <div class="col-sm-12" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      {% if link.abstract %}
      <div class="abstract" style="margin-top: 10px;">
        <details>
          <summary style="cursor: pointer; color: #007bff;">Abstract</summary>
          <p style="margin-top: 5px; text-align: justify;">{{ link.abstract }}</p>
        </details>
      </div>
      {% endif %}
    <div class="links" style="margin-top: 10px;">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
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
</li>
<br>
{% endfor %}
</ol>
</div>
