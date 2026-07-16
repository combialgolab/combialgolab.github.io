---
layout: page
title: Research
subtitle: 주요 연구 분야 소개
hero_image: ../assets/img/banner.png  
hero_height: is-medium
hero_darken: true        
show_sidebar: false
---

<style>
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

/* 이미지 비율 고정 및 자름 방지 수정 */
  .card-image img {
    object-fit: contain; /* 이미지가 잘리지 않고 정해진 영역 안에 다 들어가도록 설정 */
    width: 100%;
    height: 180px;       /* 여백을 감안하여 높이를 기존 200px에서 180px로 살짝 조절 */
    padding: 1rem 1rem 0 1rem; /* 상, 좌, 우에 여백(Padding)을 주어 테두리 잘림 완벽 방지 */
    background-color: #ffffff; /* 여백 영역의 배경을 카드 흰색 배경과 통일 */
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