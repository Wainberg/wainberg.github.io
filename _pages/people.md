---
title: "Wainberg Lab"
layout: gridlay
sitemap: false
permalink: /people
---
# Lab members
{% assign index = 1 %}
<div class="row">
{% for member in site.categories.people reversed %}
{% if member.collaborator != true %}
<div class="col-sm-3-5">
  {% if member.photo %}
  {% if member.link_to_page %}
  <a href="{{ member.url }}">
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  </a>
  {% else %}
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  {% endif %}
  {% endif %}
</div>
<div class="col-sm-2-5" style="padding-top: 15px">
    {% if member.link_to_page %}
    <a href="{{ member.url }}"><h3>{{ member.title }}</h3></a>
    {% else %}
    <h3>{{ member.title }}</h3>
    {% endif %}
    <p>{{ member.info }} <br />
    {% if member.email %}
    <i class="fas fa-envelope fa-fw"></i>&nbsp; <a href="mailto:{{ member.email }}">Email</a><br />
    {% endif %}
    {% if member.twitter %}
    <i class="fab fa-twitter fa-fw"></i>&nbsp; <a href="https://twitter.com/{{ member.twitter }}">Twitter</a><br />
    {% endif %}
    {% if member.github %}
    <i class="fab fa-github fa-fw"></i>&nbsp; <a href="https://github.com/{{ member.github }}">Github</a><br />
    {% endif %}
    {% if member.scholar %}
    <i class="fas fa-book fa-fw"></i>&nbsp; <a href="{{ member.scholar }}">Google Scholar</a>
    {% endif %}
    </p>
</div>
{% assign even_odd = index | modulo: 2 %}
{% if even_odd == 0 %}
<div class="w-100"></div>
{% endif %}
{% assign index = index | plus: 1 %}
{% endif %}
{% endfor %}
<div id="gridid" class="col-12">
<h1 id="former-lab-members">Trainee collaborators</h1>
{% assign index = 1 %}
<div class="row">
{% for member in site.categories.people reversed %}
{% if member.collaborator == true %}
<div class="col-sm-3">
  {% if member.photo %}
  <img class="img-fluid" src="{{ site.url }}{{ site.baseurl }}/images/members/{{ member.photo }}">
  {% endif %}
</div>
<div class="col-sm-3 align-self-center">
    <h3>{{ member.title }}</h3>
    <p>{{ member.info }} <br /> {{ member.lab_name }} <br /> {{ member.affiliation }}
    </p>
</div>
{% assign index = index | plus: 1 %}
{% assign even_odd = index | modulo: 2 %}
{% if even_odd == 0 %}
<div class="w-100"></div>
{% endif %}
{% endif %}
{% endfor %}
</div>
</div>
