---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: Exam-Answers
---



<h1>{{ site.short-title}} {{ site.semester }} Exam Answers</h1>

{% for exam in site.data.info.exams %}
<h2>{{ site.short-title }} {{ exam.name }}</h2>
{% assign exam_keys = exam.keys %}
{% if exam_keys.size >= 1 %}
<h4><b>Keys:</b> {{ exam.keys }}</h4>
{% else %}
<h4><b>Keys:</b> <i>Coming Soon...</i></h4>
{% endif %}
<h4><b>Covers: </b>{{ exam.content }}</h4>

{% endfor %}

<h2>STAT 100 Final Exam</h2>
{% assign exam_keys = site.data.info.final-exam-keys %}
{% if exam_keys.size >= 1 %}
<h4><b>Keys:</b> {{ exam_keys }}</h4>
{% else %}
<h4><b>Keys:</b> <i>Coming Soon...</i></h4>
{% endif %}
<h4><b>Covers: </b>{{ site.data.info.final-exam-content }}</h4>
