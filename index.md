---
title: Combinatorial Algorithms Lab
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
</style>

<div class="content">
  <h3>About Our Lab</h3>
  <p>
    우리 연구실은 <strong>그래프 이론(Graph Theory)</strong>과 <strong>조합 알고리즘(Combinatorial Algorithms)</strong>을 중점적으로 연구합니다. 현실 세계의 복잡한 문제를 수학적 모델로 추상화하고, 이를 효율적으로 해결하는 알고리즘을 개발하는 것을 목표로 합니다.
  </p>
</div>

<hr>

<div class="columns">
  
  <div class="column is-7">
    <h3>📢 Latest News</h3>
    {% assign recent_news = site.data.news | sort: "date" | reverse | slice: 0, 3 %}
    
    {% for item in recent_news %}
    <div class="box" style="margin-bottom: 1.2rem; padding: 1.2rem;">
      <p class="is-size-7 has-text-info has-text-weight-bold" style="margin-bottom: 0.3rem;">{{ item.date }}</p>
      <div class="content is-size-6" style="margin-bottom: 0;">
        {{ item.content | markdownify | remove: '<p>' | remove: '</p>' }}
      </div>
    </div>
    {% endfor %}
    
    <div class="has-text-right mt-2">
      <a href="/news/" class="button is-small is-light">소식 더보기 →</a>
    </div>
  </div>

  <div class="column is-5">
    <h3>🔍 Research Areas</h3>
    <div class="content is-size-6">
      <ul>
        <li>Graph Neural Networks (GNN)</li>
        <li>Combinatorial Optimization</li>
      </ul>
    </div>
    <a href="/research/" class="button is-link is-outlined is-fullwidth mt-4">
      연구 분야 자세히 보기
    </a>
  </div>

</div>