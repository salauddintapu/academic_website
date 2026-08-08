---
layout: page
title: News
permalink: /news/
description: News and updates
nav: true
nav_order: 3
---

<div class="news">

{% assign news = site.news | sort: "date" | reverse %}

{% for item in news %}

<div class="row mb-3">
  <div class="col-sm-2">
    {{ item.date | date: "%b %d, %Y" }}
  </div>

  <div class="col-sm-10">
    {{ item.content }}
  </div>
</div>

{% endfor %}

</div>