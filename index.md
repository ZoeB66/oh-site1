---
layout: default
title: Ana Sayfa
---
{% assign s = site.data.strings.home %}
<section class="hero">
  <div class="wrap">
    <div class="eyebrow"><span class="ring sm"></span> {{ s.hero_eyebrow }}</div>
    <h1>{{ s.hero_headline_line1 }}<br><span class="hl">{{ s.hero_headline_highlight }}</span> {{ s.hero_headline_line2 }}</h1>
    <p class="lead">{{ s.hero_lead }}</p>
    <div class="btn-row">
      <a class="btn solid" href="{{ '/studio/' | relative_url }}">{{ s.cta_primary }}</a>
      <a class="btn outline" href="{{ '/blog/' | relative_url }}">{{ s.cta_secondary }}</a>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="section-head">
      <div>
        <div class="eyebrow"><span class="ring sm"></span> {{ s.blog_section_eyebrow }}</div>
        <h2>{{ s.blog_section_title_plain }} <span class="hl blue">{{ s.blog_section_title_highlight }}</span></h2>
      </div>
      <a class="see-all" href="{{ '/blog/' | relative_url }}?kategori=pilates">{{ s.see_all }}</a>
    </div>
    <div class="cards">
      {% assign pilates_posts = site.posts | where: "published", true | where: "category", "Pilates" | limit: 3 %}
      {% for post in pilates_posts %}
      <a class="card" href="{{ post.url | relative_url }}">
        <div class="thumb" {% if post.image %}style="background-image:url('{{ post.image | relative_url }}');background-size:cover;background-position:center;opacity:1;"{% endif %}></div>
        <div class="body">
          <div class="eyebrow"><span class="ring sm"></span> {{ post.category }}</div>
          <h3>{{ post.title }}</h3>
          {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 18 }}</p>{% endif %}
          <div class="meta">{{ post.date | date: "%-d %B %Y" }}</div>
        </div>
      </a>
      {% endfor %}
    </div>
  </div>
</section>

<section class="studio">
  <div class="wrap inner">
    <div class="img"><span class="ring"></span></div>
    <div class="text">
      <div class="eyebrow"><span class="ring sm"></span> {{ s.studio_eyebrow }}</div>
      <h2>{{ s.studio_title_plain }} <span class="hl">{{ s.studio_title_highlight }}</span></h2>
      <p>{{ s.studio_text }}</p>
      <a class="btn solid" href="{{ '/studio/dersler/' | relative_url }}">{{ s.studio_cta }}</a>
    </div>
  </div>
</section>
