---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 2em 1em; background: #f5f7ff; border-radius: 4px;">
  안녕하세요 6년차 딥러닝 엔지니어 김 둘기 입니다. <br>
첫 3년은 컴퓨터 비전 분야에서 일하였고, 지금은 생성형 인공지능 분야에서 일하고 있습니다.<br>
<br>
2025년을 맞아 공부한 내용을 열심히 정리해보고자, 블로그를 개설했습니다!<br>
개발 뿐만 아니라 제가 관심 가지고 있는 분야들의 게시글을 포스팅하고자 합니다!
</p>

This digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul>
{% assign folders = site.folders %}
{% for folder in folders %}
	{{ folder.title }}
{% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>