---
layout: archive
title: "已发表文章"
permalink: /publications/
author_profile: true
---

<div style="max-width: 800px; margin: 0 auto;">

{% if site.author.googlescholar %}
  <div class="wordwrap">你也可以在 <a href="{{site.author.googlescholar}}">我的 Google Scholar 主页</a> 上找到我的文章。</div>
{% endif %}

{% include base_path %}

<!-- 期刊论文 -->
<h2>期刊论文</h2>
<hr />
{% assign journal_index = 1 %}
{% for post in site.publications reversed %}
  {% if post.venue contains "Journal" %}
    <p>
      [{{ journal_index }}] {{ post.author }}. "{{ post.title }}." 
      <i>{{ post.venue }}</i>, vol. {{ post.volume }}, no. {{ post.issue }}, {{ post.date | date: "%Y" }}, pp. {{ post.pages }}. 
      {% if post.doi %} DOI: <a href="{{ post.doi }}" target="_blank">{{ post.doi }}</a>. {% endif %}
      {% if post.paperurl %} <a href="{{ post.paperurl }}" target="_blank">[PDF]</a> {% endif %}
    </p>
    {% assign journal_index = journal_index | plus: 1 %}
  {% endif %}
{% endfor %}

<!-- 会议论文 -->
<h2>会议论文</h2>
<hr />
{% assign conf_index = 1 %}
{% for post in site.publications reversed %}
  {% if post.venue contains "Conference" %}
    <p>
      [{{ conf_index }}] {{ post.author }}. "{{ post.title }}." 
      <i>{{ post.venue }}</i>, {{ post.location }}, {{ post.date | date: "%Y" }}, pp. {{ post.pages }}. 
      {% if post.doi %} DOI: <a href="{{ post.doi }}" target="_blank">{{ post.doi }}</a>. {% endif %}
      {% if post.paperurl %} <a href="{{ post.paperurl }}" target="_blank">[PDF]</a> {% endif %}
    </p>
    {% assign conf_index = conf_index | plus: 1 %}
  {% endif %}
{% endfor %}

</div>

