<h2 id="publications">Publications</h2>

<p class="pub-scholar">Full list also on <a href="{{ site.google_scholar }}" target="_blank" rel="noopener">Google Scholar</a>.</p>

{% assign groups = "journal|Journal Articles and Archival Conference Papers,proceedings|Conference and Workshop Proceedings,talks|Peer-Reviewed Conference Presentations" | split: "," %}
{% for g in groups %}
{% assign parts = g | split: "|" %}
{% assign key = parts[0] %}
{% assign heading = parts[1] %}
{% assign items = site.data.publications[key] %}
{% if items and items.size > 0 %}
<h3 class="pub-group">{{ heading }}</h3>

<div class="pubs">
{% for pub in items %}
<p class="pub">{{ pub.citation }}{% if pub.link %} [<a href="{{ pub.link }}" target="_blank" rel="noopener">link</a>]{% endif %}{% if pub.arxiv %} [<a href="{{ pub.arxiv }}" target="_blank" rel="noopener">arXiv</a>]{% endif %}{% if pub.status %} <span class="pub-status">{{ pub.status }}</span>{% endif %}{% if pub.award %} <span class="pub-award">{{ pub.award }}</span>{% endif %}{% if pub.media %} <span class="pub-media">{{ pub.media }}</span>{% endif %}</p>
{% endfor %}
</div>
{% endif %}
{% endfor %}
