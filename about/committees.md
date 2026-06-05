---
title: Committees
subtitle: 
description: The members of the BioHackathon Europe Organising and Programme Committees
layout: page
show_sidebar: false
hero_image: /assets/img/heroes/hero-2021-crowd.webp
hero_darken: true
---

## Organising Committee

The Organising Committee is based at the [ELIXIR Hub](https://elixir-europe.org/about-us/who-we-are), with Mihail Anton and Chloè Llewellyn as Co-chairs of the Committee.

{% if site.data.organising_committee %}
<div class="columns is-multiline">
    {% for member in site.data.organising_committee %}
    <div class="column is-one-quarter">
    <figure class="box">
        <img src="{{ site.baseurl }}/assets/img/committees/{{ member.picture }}" alt="{{ member.name }}" width="200" class="has-border"/>
        <figcaption>{{ member.name }}</figcaption>
    </figure>
    </div>
    {% endfor %}
</div>
{% endif %}

## Programme Committee

{% if site.data.programme_committee %}
<table class="table is-striped mt-5">
<tr class="has-background-grey-darker">
<th class="has-text-white">Name</th>
<th class="has-text-white">Affiliation</th>
</tr>
{% for member in site.data.programme_committee %}
<tr>
<td class="has-text-weight-bold">{{ member.name }}</td>
<td>
{% if member.link %}<a href="{{ member.link }}">{% endif %}
{{ member.affiliation }}
{% if member.link %}</a>{% endif %}
</td>
</tr>
{% endfor %}
{% endif %}
