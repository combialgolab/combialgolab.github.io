---
title: Combinatorial Algorithms Lab.
subtitle: Welcome to our research group @ Inha Univ
layout: page
hero_height: is-custom
hero_image: assets/img/banner.png  
show_sidebar: true
---

<style>
.btn-responsive {
    /* 기존 인라인 스타일을 클래스로 이전 */
    background-color: #005BAC !important;
    color: #fff !important;
    height: 40px !important;
    
    /* 너비 설정: 글자 길이에 맞춤 */
    width: auto !important; 
    min-width: 160px; /* 너무 작아지지 않게 최소 너비 설정 */
    padding: 0 1.5rem !important; /* 좌우 여백 추가 */
    white-space: nowrap; /* 글자가 버튼 안에서 줄바꿈되지 않도록 설정 */
  }

/* 키워드 섹션 커스텀 스타일 */
  .keyword-container {
    display: flex;
    gap: 1.5rem;
    margin-bottom: 2rem;
  }

  .keyword-card {
    flex: 1;
    background: #f9f9f9;
    border-top: 4px solid #005BAC; /* 연구실 메인 컬러 포인트 */
    padding: 1.5rem;
    box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    transition: transform 0.2s ease;
  }

  .keyword-title {
    color: #005BAC;
    font-size: 1.25rem;
    font-weight: 700;
    margin-bottom: 1rem;
    display: block;
    border-bottom: 1px solid #ddd;
    padding-bottom: 0.5rem;
  }

  .keyword-list {
    list-style: none !important;
    margin-left: 0 !important;
    padding-left: 0 !important;
  }

  .keyword-list li {
    position: relative;
    padding-left: 1.2rem;
    margin-bottom: 0.5rem;
    font-size: 0.95rem;
    color: #4a4a4a;
  }

  .keyword-list li::before {
    content: "•";
    position: absolute;
    left: 0;
    color: #005BAC;
    font-weight: bold;
  }

  .hero.is-custom .hero-body {
    padding-top: 13rem;
    padding-bottom: 13rem; 
  }

  @media screen and (max-width: 768px) {
    .hero.is-custom .hero-body {
      padding-top: 6rem;
      padding-bottom: 6rem;
    }
    .keyword-container {
      flex-direction: column; /* 세로 정렬로 변경 */
      gap: 1rem; /* 세로로 쌓일 때 카드 사이 간격 */
    }

    .keyword-card {
      width: 100%; /* 모바일에서 가로 너비를 꽉 채움 */
    }

    .btn-responsive {
      display: flex !important; /* 모바일에서는 한 줄을 다 쓰도록 변경 */
      width: 100% !important;
      margin: 0 auto;
    }
  }

  /* 세로 섹션 간 간격 조절 */
  .vertical-section {
    margin-bottom: 4rem;
  }
</style>

<style>
.two-col {
  display: flex;
  gap: 40px;
}

.two-col p {
  width: 50%;
}
</style>

<div class="content">
  <h3>About Our Lab</h3>
  <p>
    우리 연구실은 <strong>구조적 그래프 이론(Structural Graph Theory)</strong>과 <strong>조합적 알고리즘(Combinatorial Algorithms)</strong>을 중점적으로 연구합니다. 산업 혹은 컴퓨터과학에서 등장하는 복잡한 문제를 이산적 모델인 그래프, 행렬 등으로 추상화하고 이를 효율적으로 해결하는 알고리즘의 설계를 목표로 합니다.
  </p>

  <hr>

  <h3>Keywords</h3>
 <div class="keyword-container">
  <div class="keyword-card">
    <strong class="keyword-title">Structural Graph Theory</strong>
    <ul class="keyword-list">
      <li>Graph parameters</li>
      <li>Graph decompositions</li>
      <li>Forbidden structures</li>
      <li>Sparse/dense graph classes</li>
    </ul>
  </div>

  <div class="keyword-card">
    <strong class="keyword-title">Combinatorial Algorithms</strong>
    <ul class="keyword-list">
      <li>Parameterized complexity</li>
      <li>Kernelization</li>
      <li>Approximation algorithms</li>
      <li>Combinatorial optimization</li>
    </ul>
  </div>
</div>
   <a href="/research/" class="button is-link is-outlined btn-responsive">
    연구 분야 보기
  </a>
</div>

<hr>


<div class="content">
  <h3>Recent Publications</h3>
  {% assign recent_pubs = site.data.publications | slice: 0, 3 %}

  {% for paper in recent_pubs %}
    <div class="box" style="margin-bottom: 1.2rem; padding: 1.2rem;">
      <p class="is-size-6 has-text-weight-bold" style="margin-bottom: 0.2rem; line-height: 1.3;">
        {{ paper.title }}
      </p>
      <p class="is-size-7 has-text-grey" style="margin-bottom: 0.2rem;">
        {{ paper.authors | markdownify | remove: '<p>' | remove: '</p>' }}
      </p>
      <p class="is-size-7 has-text-link is-italic" style="margin-bottom: 0;">
        {{ paper.venue }} ({{ paper.year }})
      </p>
    </div>
  {% endfor %}
  <a href="/publications/" class="button is-link is-outlined btn-responsive">
    논문 전체 보기
  </a>
</div>
