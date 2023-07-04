---
title: "Wainberg Lab"
layout: default
sitemap: false
permalink: /
---
<div class="col-sm-12">
<div class="bigtitle titlebox">
Welcome to the Wainberg lab!
</div>
</div>

<div class="col-sm-12">
  <p> We apply statistics, machine learning and other computational approaches to large datasets to learn how genetics causes brain diseases. </p>
  <p> Our overarching goal is to find new drug targets, while developing new ways to do genetic studies and extract meaning from them along the way. </p>
  <p> We are part of the <a href="https://net.lunenfeld.ca/pcphr/">Prosserman Centre for Population Health Research</a> at Mount Sinai Hospital, affiliated with the University of Toronto. </p>
</div>

<div class="col-12">
<div class="carousel slide" data-ride="carousel">
  <div class="carousel-inner" role="listbox">
    {% for image in site.data.gallery %}
    {% if forloop.index == 1 %}
    <div class="carousel-item active">
    {% else %}
    <div class="carousel-item">
    {% endif %}
      <img class="d-block w-100" src="{{ site.url }}{{ site.baseurl }}/images/carousel/{{ image.name }}" alt="{{ image.alt }}">
    </div>
    {% endfor %}
  </div>
</div>
</div>
