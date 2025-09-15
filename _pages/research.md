---
layout: default
title: research
permalink: /research/
nav: true
nav_order: 1
project_categories: [Compressive multidimensional imaging, Physics-informed machine learning, Robust and trustworthy imaging]

---

<h1 class="post-title">research </h1>
Some of our previous projects are summarized below.

<div>
{%- for category in page.project_categories %}
{%- assign categorized_projects = site.data.past_projects | where: "category", category -%}
{%- assign sorted_projects = categorized_projects | sort: "importance" -%}
{%- assign categorized_descriptions = site.data.past_projects_description | where: "category", category -%}
<h3>{{category}}</h3>
{%- for descrip in categorized_descriptions -%}
<p>{{descrip.description}} </p>
{% endfor %}

<div class="row">
	{%- for project in sorted_projects -%}
		<div class="col-sm mt-3 mt-md-0">
		<a href="{{project.website}}">
	    {% if project.img contains 'mp4' -%}
		{% include video.html 
			path=project.img
			class="img-fluid z-depth-1 rounded" 
			controls=true autoplay=true muted=true caption = project.name%}
		{%- else -%}
		{% include figure.html path=project.img caption = project.name class="img-fluid rounded z-depth-1" %}
		{%- endif %}
	</a>
	</div>
	{% endfor %}
	
</div>
{% endfor %}
</div>

Check out our recent papers for more details (see <a href='../publications'>publications</a>). 

