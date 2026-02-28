---
layout: page
title: Research Areas
subtitle: 주요 연구 분야 소개
hero_image: ../assets/img/banner.png  
hero_height: is-medium
hero_darken: true        
show_sidebar: false
---

<style>
  /* 쇼핑몰처럼 보이게 하는 마법의 CSS */
  .research-card {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
    height: 100%; /* 카드 높이 통일 */
    border-radius: 8px; /* 둥근 모서리 */
    overflow: hidden;
  }
  
  /* 마우스 올렸을 때 살짝 떠오르는 효과 */
  .research-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  }

  /* 이미지 비율 고정 (쇼핑몰 썸네일처럼) */
  .card-image img {
    object-fit: cover;
    width: 100%;
    height: 200px; /* 원하는 높이로 조절 가능 */
  }

  /* 카드 내부 여백 */
  .card-content {
    padding: 1.5rem;
  }
</style>

<div class="columns is-multiline">
  
  {% for item in site.data.research %}
  <div class="column is-4">
    <a href="{{ item.link }}">
      <div class="card research-card">
        <div class="card-image">
          <figure class="image">
            <img src="{{ item.image }}" alt="{{ item.title }}">
          </figure>
        </div>
        <div class="card-content">
          <p class="title is-5">{{ item.title }}</p>
          <p class="subtitle is-6 has-text-grey">{{ item.subtitle }}</p>
          <div class="content is-small">
            {{ item.description }}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endfor %}
  </div>