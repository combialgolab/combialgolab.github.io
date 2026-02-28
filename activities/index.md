---
layout: page
title: Activities
subtitle: 학회 참석 및 연구실 행사
hero_image: ../assets/img/banner.png  
hero_height: is-medium
hero_darken: true         
show_sidebar: false
---

<style>
  /* 사진 카드 스타일 */
  .activity-card {
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    transition: transform 0.2s;
    height: 100%; 
    background-color: #fff;
    color: #363636; /* 링크 기본 파란색 방지 */
  }
  .activity-card:hover {
    transform: translateY(-5px); 
    box-shadow: 0 10px 15px rgba(0,0,0,0.15);
  }
  .activity-caption {
    padding: 12px; 
    text-align: center;
    font-weight: 600;
    font-size: 0.9rem; 
  }
  .activity-caption small {
    display: block; 
    margin-top: 5px;
  }
  /* a 태그 호버 시 텍스트 밑줄 생기는 현상 방지 */
  a:hover .activity-caption {
    text-decoration: none;
  }
</style>

<div class="columns is-multiline">

  {% for item in site.data.activities %}
  <div class="column is-3"> 
    <a href="{{ item.link }}">
      <div class="activity-card">
        <figure class="image is-4by3">
          <img src="{{ item.image }}" alt="{{ item.title }}" style="object-fit: cover; width: 100%; height: 100%;">
        </figure>
        <div class="activity-caption">
          {{ item.title }}
          <small class="has-text-grey">
            {{ item.date }}
            {% if item.location != "" %}
              • {{ item.location }}
            {% endif %}
          </small>
        </div>
      </div>
    </a>
  </div>
  {% endfor %}

</div>