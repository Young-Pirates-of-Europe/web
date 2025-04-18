---
layout: home
title: Young Pirates of Europe
---
<section id="who-we-are">
<div>  
  <h1>Sailing For Democracy<br />Fighting for freedom</h1>
  <p>
      {{site.description}}
  </p>
</div>


<aside id="newsbox">
  <h2>News</h2>
  <ul>
    {% for post in site.posts limit:3 %}
    <li>
      <h3>{{ post.date | date: "%d-%m-%Y" }}</h3>
      {{ post.content }}
    </li>
    {% endfor %}
  </ul>
</aside>
</section>

<section id="member-organisations">
  <h2>Member Organisations</h2>
  <ul>
    {% for member in site.data.mo %}
    <li>
      <div class="mo-pic"><img src="{{ member.pic }}" /></div>
      <div class="mo-info">
        <h3>{{ member.name }}</h3>
        <h4>{{ member.country }}</h4>
      </div>
      <div class="mo-icons">
        <a href="mailto:{{member.email}}">
            <span class="grey fa-solid fa-envelope fa-lg"></span>
        </a>
        {%- for entry in member.social_links -%}
        <a rel="me" href="{{ entry.url }}" target="_blank" title="{{ entry.title }}">
            <span class="grey fa-brands fa-{{ entry.icon }} fa-lg"></span>
        </a>
        {%- endfor -%}
      </div>
    </li>
    {% endfor %}
  </ul>
</section>

<section id="board">
  <h2>The Board</h2>
  <ul class="outer">
    <li class="inner">
      {% for member in site.data.board limit: 3 %}
      <div>
        <img src="{{ member.pic }}" />
        <h3>{{ member.name }}</h3>
        <h3>{{ member.role }}</h3>
        <p>{{ member.country }}</p>
      </div>
      {% endfor %}
    </li>
    <li class="inner">
      {% for member in site.data.board limit: 3 offset: 3%}
      <div>
        <img src="{{ member.pic }}" />
        <h3>{{ member.name }}</h3>
        <h3>{{ member.role }}</h3>
        <p>{{ member.country }}</p>
      </div>
      {% endfor %}
    </li>
  </ul>
</section>

<section id="transparency">
  <h2>Transparency</h2>
  <ul>
    {% for item in site.data.transparency %}
    <li>
      <h3>{{ item.title }}</h3>
      {{ item.description }} <br />
      <a href="{{item.url}}">{{ item.linktext }}</a>
    </li>
    {% endfor %}
  </ul>
</section>

<section id="contact">
  <div class="contact-wrapper">
    <div>
      <h2>Contact</h2>
      <h3>Name</h3>
      Young Pirates of Europe a.s.b.l. <br />
      (also known as YPE)
      <h3>Address</h3>
      1a, Route de Luxembourg L - 8184 Kopstal Luxembourg
      <h3>ID</h3>
      F10614 registered in R.C.S Luxembourg
      <br />
    </div>
    <div class="main-socials">
      <a href="mailto:young-pirates.eu"><span class="grey fa-solid fa-envelope fa-3x"></span></a>
      <a href="https://www.facebook.com/youngpiratesEU/"><span class="grey fa-brands fa-facebook fa-3x"></span></a>
      <a href="https://www.instagram.com/youngpirateseu/"><span class="grey fa-brands fa-instagram fa-3x"></span></a>
    </div>
  </div>
</section>
