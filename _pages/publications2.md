---
title: "iSMART Lab - Publications"
layout: gridlay
excerpt: "iSMART Lab -- Publications."
sitemap: false
permalink: /publications2/
---

# Publications

## Group highlights

(For full list of publications and patents see [Google Scholar](https://scholar.google.com/citations?hl=en&user=V8pn4tIAAAAJ&view_op=list_works&sortby=pubdate))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

<div class="row">

 <div class="col-sm-12 clearfix">
  <div class="well">
   <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="25%" style="aspect-ratio: 1.8;float: left" />
   <pubtit>{{ publi.title }}</pubtit>
   <p><em>{{ publi.authors }}</em></p>
   <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
   <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
   <p> {{ publi.news2 }}</p>
  </div>
 </div>

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
{% endif %}

<p> &nbsp; </p>



## Selected publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
