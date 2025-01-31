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


<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
	{% assign path_parts = note.path | split: '/' %}
	{% assign folder_name = path_parts[1] %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ folder_name }}/{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul>
{% for file in site.notes %}
	{% assign path_parts = file.path | split: '/' %}
	{% assign folder_name = path_parts[1] %}
	 <li>{{ path_parts }}</li>
{% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>