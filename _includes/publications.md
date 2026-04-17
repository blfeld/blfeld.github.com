<h2 id="Working Paper">Working Paper</h2>
<div class="publications">
<ol class="bibliography">
{% for link in site.data.publications.main %}
<li>
<div class="pub-row">
  <div class="col-sm-12" style="position: relative;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div style="margin-top: 10px; display: flex; gap: 1.2rem; align-items: baseline;">
        {% if link.abstract %}
        <details>
          <summary class="abstract-toggle">Abstract</summary>
          <p style="margin-top: 5px; text-align: justify;">{{ link.abstract }}</p>
        </details>
        {% endif %}
        {% if link.pdf %}
        <a href="{{ link.pdf }}" target="_blank">PDF</a>
        {% endif %}
        {% if link.page %}
        <a href="{{ link.page }}" target="_blank">Project Page</a>
        {% endif %}
        {% if link.coverage %}<span>Coverage: {{ link.coverage }}</span>{% endif %}
        {% if link.presentations %}<span>Presentations: {{ link.presentations }}</span>{% endif %}
        {% if link.others %}{{ link.others }}{% endif %}
      </div>
  </div>
</div>
</li>
<br>
{% endfor %}
</ol>
</div>
