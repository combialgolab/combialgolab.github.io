---
layout: page
title: Publications
subtitle: 논문 및 학술 발표
hero_image: ../assets/img/banner.png  
hero_height: is-medium
hero_darken: true         
show_sidebar: false
---

<style>
  .pub-item {
    margin-bottom: 1.5rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid #eee; 
  }
  .pub-title {
    font-size: 1.1rem;
    font-weight: 700;
    color: #363636;
    margin-bottom: 0.3rem;
  }
  .pub-authors {
    color: #666;
    margin-bottom: 0.3rem;
  }
  /* 이름 으로 마크다운 작성 시 기존의 .my-name 클래스와 동일한 스타일이 적용되도록 설정 */
  .pub-authors strong {
    font-weight: 900; 
    color: #363636;
  }
  .pub-venue {
    font-style: italic;
    color: #005BAC; 
    font-weight: 500;
    margin-bottom: 0.2rem;
  }
  .pub-date {
    font-size: 0.9rem;
    color: #7a7a7a;
    margin-bottom: 0.5rem;
  }
</style>
{% assign category_order = "Preprints, Accepted Journal Papers, Refereed Conference Papers" | split: ", " %}

{% for category in category_order %}
{% assign category_papers = site.data.publications | where: "type", category %}
{% if category_papers.size > 0 %}
<h2 class="title is-4" {% if forloop.first == false %} {% endif %}>
{{ category }}
</h2>

{% for paper in category_papers %}
<div class="pub-item">
<div class="pub-title">
{% if paper.link %}
<a href="{{ paper.link }}" target="_blank" style="color: inherit;">{{ paper.title | markdownify | remove: '<p>' | remove: '</p>' }}</a>
{% else %}
{{ paper.title | markdownify | remove: '<p>' | remove: '</p>' }}
{% endif %}
</div>
      
<div class="pub-authors">
{{ paper.authors | markdownify | remove: '<p>' | remove: '</p>' }}
</div>
      
<div class="pub-venue">
{{ paper.venue | markdownify | remove: '<p>' | remove: '</p>' }}
</div>

<div class="pub-date">
{{ paper.date_detail | default: paper.year }}
</div>

<div class="tags is-marginless" style="margin-top: 0.5rem;">
{% if paper.pdf %}
<a href="{{ paper.pdf }}" class="tag is-link is-light">PDF</a>
{% endif %}

{% if paper.code %}
<a href="{{ paper.code }}" class="tag is-info is-light">Code</a>
{% endif %}

{% if paper.award %}
<span class="tag is-warning is-light">{{ paper.award }}</span>
{% endif %}
</div>
</div>
{% endfor %}
{% endif %}
{% endfor %}