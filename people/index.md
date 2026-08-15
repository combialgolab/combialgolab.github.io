---
layout: page
title: People
subtitle: 연구실 구성원 소개
hero_image: ../assets/img/banner.png  
hero_height: is-medium
hero_darken: true              
show_sidebar: false
---

<style>
  /* 프로필 이미지 스타일 */
  .profile-img {
    object-fit: cover;
    width: 100%;
    height: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1); /* 사진에 살짝 그림자 추가 */
  }
  
  .member-box {
    margin-bottom: 2rem;
  }
  
  /* 텍스트 스타일 (기본보다 크게 설정) */
  .member-name {
    font-weight: 600; /* 더 굵게 */
    color: #363636;
    margin-bottom: 0.2rem;
  }
  .member-role {
    color: #005BAC; /* 딥 블루 포인트 */
    font-weight: 500;
    margin-bottom: 0.5rem;
  }
</style>

{% assign professors = site.data.people | where: "group", "professor" %}
{% if professors.size > 0 %}
<h2 class="title is-3">Professor</h2>
<div class="columns is-multiline">
  {% for member in professors %}
  <div class="column is-12">
    <div class="columns">
      <div class="column is-3">
        <figure class="image is-square">
          <img src="{{ member.img }}" alt="{{ member.name }}" class="profile-img">
        </figure>
      </div>
      <div class="column">
        <div class="member-name is-size-4">{{ member.name }}</div>
        <p class="member-role is-size-5">{{ member.role }}</p>
        
        <div class="content is-size-6">
          {% if member.interests %}
          <p class="mb-1"><strong>연구 분야:</strong> {{ member.interests }}</p>
          {% endif %}
          {% if member.email %}
          <p class="mb-1"><strong>이메일:</strong> {{ member.email }}</p>
          {% endif %}
          {% if member.location %}
          <p class="mb-1"><strong>위치:</strong> {{ member.location }}</p>
          {% endif %}
        </div>

        {% if member.website %}
        <a href="{{ member.website }}" target="_blank" class="button is-outlined is-info is-small">
          🏠 Personal Website
        </a>
        {% endif %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
<hr>
{% endif %}


{% assign researchers = site.data.people | where: "group", "researcher" %}
{% if researchers.size > 0 %}
<h2 class="title is-3">Researchers</h2>
<div class="columns is-multiline">
  {% for member in researchers %}
  <div class="column is-6 member-box">
    <div class="columns is-mobile">
      
      <div class="column is-4">
        <figure class="image is-square">
          <img src="{{ member.img }}" alt="{{ member.name }}" class="profile-img">
        </figure>
      </div>
      
      <div class="column">
        <div class="member-name is-size-4">{{ member.name }}</div>
        <div class="member-role is-size-6">{{ member.role }}</div>
        
        {% if member.interests %}
          <p class="mb-1"><strong>연구 분야:</strong> {{ member.interests }}</p>
          {% endif %}
          {% if member.email %}
          <p class="mb-1"><strong>이메일:</strong> {{ member.email }}</p>
          {% endif %}
          {% if member.location %}
          <p class="mb-1"><strong>위치:</strong> {{ member.location }}</p>
          {% endif %}

          {% if member.website %}
        <a href="{{ member.website }}" target="_blank" class="button is-outlined is-info is-small">
          🏠 Personal Website
        </a>
        {% endif %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
<hr>
{% endif %}


{% assign graduate = site.data.people | where: "group", "graduate" %}
{% if graduate.size > 0 %}
<h2 class="title is-3">Graduate Students</h2>
<div class="columns is-multiline">
  {% for member in graduate %}
  <div class="column is-6 member-box">
    <div class="columns is-mobile">
      
      <div class="column is-4">
        <figure class="image is-square">
          <img src="{{ member.img }}" alt="{{ member.name }}" class="profile-img">
        </figure>
      </div>
      
      <div class="column">
        <div class="member-name is-size-4">{{ member.name }}</div>
        <div class="member-role is-size-6">{{ member.role }}</div>
        
        {% if member.interests %}
          <p class="mb-1"><strong>연구 분야:</strong> {{ member.interests }}</p>
          {% endif %}
          {% if member.email %}
          <p class="mb-1"><strong>이메일:</strong> {{ member.email }}</p>
          {% endif %}
          {% if member.location %}
          <p class="mb-1"><strong>위치:</strong> {{ member.location }}</p>
          {% endif %}

          {% if member.website %}
        <a href="{{ member.website }}" target="_blank" class="button is-outlined is-info is-small">
          🏠 Personal Website
        </a>
        {% endif %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
<hr>
{% endif %}


{% assign undergraduate = site.data.people | where: "group", "undergraduate" %}
{% if undergraduate.size > 0 %}
<h2 class="title is-3">Undergraduate Students</h2>
<div class="columns is-multiline">
  {% for member in undergraduate %}
  <div class="column is-6 member-box">
    <div class="columns is-mobile">
      
      <div class="column is-4">
        <figure class="image is-square">
          <img src="{{ member.img }}" alt="{{ member.name }}" class="profile-img">
        </figure>
      </div>
      
      <div class="column">
        <div class="member-name is-size-4">{{ member.name }}</div>
        <div class="member-role is-size-6">{{ member.role }}</div>
        
        {% if member.interests %}
          <p class="mb-1"><strong>연구 분야:</strong> {{ member.interests }}</p>
          {% endif %}
          {% if member.email %}
          <p class="mb-1"><strong>이메일:</strong> {{ member.email }}</p>
          {% endif %}
          {% if member.location %}
          <p class="mb-1"><strong>위치:</strong> {{ member.location }}</p>
          {% endif %}

          {% if member.website %}
        <a href="{{ member.website }}" target="_blank" class="button is-outlined is-info is-small">
          🏠 Personal Website
        </a>
        {% endif %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
<hr>
{% endif %}


{% assign alumni = site.data.people | where: "group", "alumni" %}
{% if alumni.size > 0 %}
<h2 class="title is-3">Alumni</h2>
<div class="table-container">
  <table class="table is-fullwidth is-hoverable">
    <thead>
      <tr>
        <th>Name</th>
        <th>Period</th>
        <th>Current Affiliation</th>
      </tr>
     </thead>
     <tbody>
      {% for member in alumni %}
      <tr>
        <td><strong>{{ member.name }}</strong></td>
        <td>{{ member.period }}</td>
        <td>{{ member.destination }}</td>
      </tr>
      {% endfor %}
     </tbody>
  </table>
</div>
<hr>
{% endif %}