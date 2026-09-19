<h2 id="selected-publications">Selected Publications</h2>

{% assign all = site.data.publications.journal | concat: site.data.publications.proceedings %}
{% for group in site.data.publications.selected %}
<h3 class="pub-group">{{ group.heading }}</h3>

<div class="pubs">
{% for id in group.ids %}
{% for pub in all %}
{% if pub.id == id %}
<p class="pub">{{ pub.citation }}{% if pub.link %} [<a href="{{ pub.link }}" target="_blank" rel="noopener">link</a>]{% endif %}{% if pub.status %} <span class="pub-status">{{ pub.status }}</span>{% endif %}{% if pub.award %} <span class="pub-award">{{ pub.award }}</span>{% endif %}{% if pub.media %} <span class="pub-media">{{ pub.media }}</span>{% endif %}</p>
{% endif %}
{% endfor %}
{% endfor %}
</div>
{% endfor %}

<p class="sel-more">See <a href="{{ '/publications/' | relative_url }}">full publication list</a>.</p>
