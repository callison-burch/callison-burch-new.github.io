---
title: Publications
layout: default
active_tab: publications
---


<table class="table"> 
<tbody>
  {% for year in (2000..2023) reversed %}
    <tr><td>
		<a name="{{year}}"></a><h1>{{year}}</h1>
    </td></tr>
    {% for publication in site.data.publications %}
    	{% if publication.year == year %}
    	<tr>
      	<td>
				{% if publication.url %}
					<a href="{{ publication.url }}">{{ publication.title }}.</a>
        {% else %}
					{{ publication.title }}.
				{% endif %}
				{% if publication.award %}
					<b>{{ publication.award }}.</b>
				{% endif %}
				{{ publication.authors }}.
				{{ publication.venue }}  {{ publication.year }}.
				</td>
			</tr>
			{% endif %}
		{% endfor %}
	{% endfor %}
</tbody>
</table>
