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
  }
</style>

{% assign grouped_papers = site.data.publications | group_by: "year" | sort: "name" | reverse %}

{% for year_group in grouped_papers %}
  
  <h2 class="title is-4" {% if forloop.first == false %}style="margin-top: 3rem;"{% endif %}>
    {{ year_group.name }}
  </h2>

  {% for paper in year_group.items %}
  <div class="pub-item">
    <div class="pub-title">
      {{ paper.title }}
    </div>
    
    <div class="pub-authors">
      {{ paper.authors | markdownify | remove: '<p>' | remove: '</p>' }}
    </div>
    
    <div class="pub-venue">
      {{ paper.venue }}
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

{% endfor %}