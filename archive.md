---
layout: page
title: Archive
permalink: /archive/
---
<div>
  {% for post in site.posts %}
  	{% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
  	{% if currentyear != year %}
    	{% unless forloop.first %}</ul></div>{% endunless %}
    		<div style="padding:0px 0px 16px 0px"><p>{{ currentyear }}</p>
    		<ul>
    		{% capture year %}{{currentyear}}{% endcapture %} 
  		{% endif %}
    <li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
{% endfor %}
</div>