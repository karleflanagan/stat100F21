---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: Exam-Schedule
---



<h1>{{ site.short-title}} {{ site.semester }} Exam Schedule</h1>
<h4><b style="color:red;">Important Info:</b>
<ul>
    <li>All Stat 100 Exams for all sections (both in person and online sections) will be in person unless the university changes to online. Plan on coming in person!</li>
    <li>There will be three midterm exams and a comprehensive final exam.</li>
    <li>Because all exams are in person, students are allowed to miss one of the 3 midterm exams without any penalty. It is in your best interest to take all 3 midterm exams, however, if you are sick or cannot take one of them for whatever reason, this will not hurt your grade.</li>
    <li>If you miss an exam, whatever score you get on the final exam will be put in for your missed exam score.</li>
    <li>The final exam is mandatory! Everyone must take the final.</li>
    <li>Exam Locations will be posted closer to the dates.</li>
    <li>If you are not in Champaign-Urbana, please contact me immediately to discuss exams.</li>
</ul>
</h4>

{% for exam in site.data.info.exams %}
<h2>{{ site.short-title }} {{ exam.name }}</h2>
{% assign exam_keys = exam.keys %}
{% if exam_keys.size >= 1 %}
<h4><b>Keys:</b> {{ exam.keys }}</h4>
{% endif %}
<h4><b>Date:</b> {{ exam.date }}</h4>
<h4><b>Time: </b>{{ exam.time }}</h4>
<h4><b>Covers: </b>{{ exam.content }}</h4>

<!-- Insert Exam number (e.g. 'Exam1') -->
{% if exam.base-name == 'Exam1' %}
<h4><b>Locations: </b> {{ exam.locations }}</h4>
{% include exam_schedule.html %}
<h4><b>Conflict Exam:</b> {{ exam.conflict }}</b></h4>
    <li>Location for <b>ALL STUDENTS</b> with Last Names starting with <b>A-L</b>: <a href="http://ada.fs.illinois.edu/0043.html" target="_blank">Gregory Hall (Room 100)</a><br></li>
    <li>Location for <b>ALL STUDENTS</b> with Last Names starting with <b>M-Z</b>: <a href="http://ada.fs.illinois.edu/0158.html" target="_blank">Bevier Hall (Room 180)</a><br></li></ul>
{% endif %}
{% endfor %}

<!-- <h2>Final Exam</h2>
<ul>
<li>
 I use the final exam time assigned to our class by the university.<br>
</li>
<li>
See <b><a href="{{ site.data.info.uiucfinals }}" target="\_blank">Official University Final Exams Schedules and Policies</a></b>.<br>
</li> 
<li>
The final cumulative for Chapters 1-24 <b>(ALL chapters in notebook)</b><br>
</li>
</ul>-->

{% include final-schedule.html %}


