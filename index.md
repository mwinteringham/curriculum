---
layout: default
---

<div class="row">
  <div class="col-sm-12">
    <h2>Curriculum topics</h2>
    <p>Select one to view learning outcomes for the topic</p>
  </div>
</div>
<div class="row">
{% for topic in site.topics %}
{% assign loopindex = forloop.index | modulo: 4 %}
{% if loopindex != 0 %}
    <div class="col-sm-3 topic">
      <p><a href="{{ site.baseurl }}{{topic.url}}">{{ topic.name}}</a></p>
    </div>
{% else %}
    <div class="col-sm-3 topic">
      <p><a href="{{ site.baseurl }}{{topic.url}}">{{ topic.name}}</a></p>
    </div>
  </div>
  <div class="row">
{% endif %}
{% endfor %}
</div>