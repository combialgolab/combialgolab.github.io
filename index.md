---
title: Combinatorial Algorithms Lab.
subtitle: Welcome to our research group @ Inha Univ
layout: page
hero_height: is-custom
hero_image: assets/img/banner.png  
show_sidebar: true
---

<style>
  .hero.is-custom .hero-body {
    padding-top: 13rem;
    padding-bottom: 13rem; 
  }

  @media screen and (max-width: 768px) {
    .hero.is-custom .hero-body {
      padding-top: 6rem;
      padding-bottom: 6rem;
    }
  }

  /* 세로 섹션 간 간격 조절 */
  .vertical-section {
    margin-bottom: 4rem;
  }
</style>

<div class="content">
  <h3>About Our Lab</h3>
  <p>
    우리 연구실은 <strong>구조적 그래프 이론(Structural Graph Theory)</strong>과 <strong>조합적 알고리즘(Combinatorial Algorithms)</strong>을 중점적으로 연구합니다. 산업 혹은 컴퓨터과학에서 등장하는 복잡한 문제를 이산적 모델인 그래프, 행렬 등으로 추상화하고 이를 효율적으로 해결하는 알고리즘의 설계를 목표로 합니다.


    우리 연구실은 <strong>그래프 이론(Graph Theory)</strong>과 <strong>조합 알고리즘(Combinatorial Algorithms)</strong>을 중점적으로 연구합니다. 현실 세계의 복잡한 문제를 수학적 모델로 추상화하고, 이를 효율적으로 해결하는 알고리즘을 개발하는 것을 목표로 합니다.
  </p>
  <h3>Keywords</h3>
  <p>
    <strong>Structural Graph Theory</strong>

    -Graph parameters
    -Graph decompositions
    -forbidden structures
    -sparse/dense graph classes
  </p>
  <p>
    <strong>Combinatorial Algorithms</strong>
    -NP-completeness
    -Parameterized complexity
    -Kernelization
    -Approximation algorithms
    -Combinatorial Optimization
  </p>
   <a href="/research/" class="button is-link is-outlined" style="width: 20%; background-color: #005BAC; color: #fff; height: 40px;">
    연구 분야 자세히 보기
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
  <a href="/publications/" class="button is-link is-outlined" style="width: 20%; background-color: #005BAC; color: #fff; height: 40px;">
    논문 전체 보기
  </a>
</div>
