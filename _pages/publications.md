---
layout: default
title: "已发表论文"
permalink: /publications/
author_profile: true
---

{% if site.talkmap_link == true %}

<p style="text-decoration:underline;"><a href="/talkmap.html">See a map of all the places I've given a talk!</a></p>

{% endif %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}


已发表论文列表

期刊论文

[1] 你的名字, 其他作者. "论文标题." 期刊名称, vol. 期刊卷号, no. 期刊期号, YYYY, pp. 起始页码-终止页码. DOI: [DOI链接]

[2] 你的名字, 其他作者. "论文标题." 期刊名称, vol. 期刊卷号, no. 期刊期号, YYYY, pp. 起始页码-终止页码. DOI: [DOI链接]
