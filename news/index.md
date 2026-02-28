---
layout: page
title: News
subtitle: 연구실 주요 소식
hero_image: ../assets/img/banner.png  
hero_height: is-medium
hero_darken: true         
show_sidebar: false
---

<style>
  .news-date {
    font-weight: bold;
    color: #005BAC; 
    min-width: 100px;
    display: inline-block;
  }
  .news-item {
    padding: 10px 0;
    border-bottom: 1px solid #eee;
  }
</style>

{% assign grouped_news = site.data.news | group_by: "year" | sort: "name" | reverse %}

{% for year_group in grouped_news %}
  
  <h3 class="title is-4" {% if forloop.first == false %}style="margin-top: 3rem;"{% endif %}>
    {{ year_group.name }}
  </h3>

  {% for item in year_group.items %}
  <div class="news-item">
    <span class="news-date">{{ item.date }}</span>
    <span>{{ item.content | markdownify | remove: '<p>' | remove: '</p>' }}</span>
  </div>
  {% endfor %}

{% endfor %}