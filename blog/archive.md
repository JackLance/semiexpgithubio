---
layout: default
title: Blog - Archive

---
{% assign dep = {{{{page.url | split:"/"}} | size }} %}{% assign dep = {{dep | minus:2 }} %}{% assign relative = '' %}{% for i in (1..dep) %}{% assign relative = {{relative | append:'../'}}%}{% endfor %}
## Archive
<ul>
{% for post in site.posts limit:5 %}
  <li>
    <a href="{{relative}}{{ post.url | replace_first:'/',''}}">{{ post.date | date:'%Y-%m-%d'}} : {{ post.title }}</a>
  </li>
{% endfor %}
</ul>