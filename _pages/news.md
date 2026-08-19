---
layout: page
title: News
permalink: /news/
nav: false
nav_order: 3
---

<div class="news">

{% assign news = site.news | sort: "date" | reverse %}

{% for item in news %}

<div class="row mb-3">
  <div class="col-sm-2">
    <strong>{{ item.date | date: "%b %d, %Y" }}</strong>
  </div>

  <div class="col-sm-10">
    {{ item.content }}
  </div>
</div>

{% endfor %}

</div>
