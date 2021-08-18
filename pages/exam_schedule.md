---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: Exam-Schedule
---



<h1>{{ site.short-title}} {{ site.semester }} Exam Schedule</h1>
<h4><b style="color:red;">Important Info:</b> There will be three midterm exams and a comprehensive final exam. All of these will be taken online on Compass 2g individually.  You can use any resources except other people.  Please be honest and make sure that your work is your work only!  There will be NO makeup exams. If you miss an exam and have written proof of a valid reason, then we will substitute your final exam score for the missed exam.
<h4>

{% for exam in site.data.info.exams %}
<h2>{{ site.short-title }} {{ exam.name }}</h2>
{% assign exam_keys = exam.keys %}
{% if exam_keys.size >= 1 %}
<h4><b>Keys:</b> {{ exam.keys }}</h4>
{% endif %}
<h4><b>Date:</b> {{ exam.date }}</h4>
<h4><b>Time: </b>{{ exam.time }}</h4>
<h4><b>Covers: </b>{{ exam.content }}</h4>

<!-- {% if exam.base-name == 'Exam2' %}
<h4><b>Locations: </b> {{ exam.locations }}</h4>
{% include exam_schedule.html %}
<h4><b>Conflict Exam: {{ exam.conflict }}</b></h4>
{% endif %} -->

{% endfor %}

<h2>Final Exam</h2>
<ul>
<!-- <li>
 I use the final exam time assigned to our class by the university.<br>
</li>
<li>
See <b><a href="{{ site.data.info.uiucfinals }}" target="\_blank">Official University Final Exams Schedules and Policies</a></b>.<br>
</li> -->
<li>
The final cumulative for Chapters 1-24 <b>(ALL chapters in notebook)</b><br>
</li>
</ul>

{% include final-schedule.html %}

<h4><b>Conflict Exam Info:</b> For exams 1-3 there will be a conflict for international students at 11pm CST on the same day.  There will also be a main conflict from 4:30-6pm those days for any students who want to sign up!  Sign up for these conflict exams on Lon Capa.  If you are taking the regular exam at 6pm, no need to sign up!</h4>