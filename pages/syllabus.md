---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: content
title: syllabus
---

# {{ site.short-title }} Syllabus {{ site.semester }} <a href="{{ site.baseurl }}/assets/docs/{{ site.short-semester }}_Stat100_Syllabus.pdf" target="\_blank">(View PDF)</a>

[Read The Syllabus]({{ site.baseurl }}/assets/img/D203723A-9034-4CE1-862C-D6B2D1F34975.jpeg)

## Instructor Contact Information
<ul>
{% for instructor in site.data.info.instructors %}
{% assign section_temp = site.data.info.sections | where: 'instructor', instructor.name %}

  <li>
     <b>{% assign type_temp = section_temp | where: 'type', 'In Person' %}
     {% if type_temp.size > 0 %}
       {% assign count = 1 %}
       {% if type_temp.size == 2 %}{% for class in type_temp %}{% if class == type_temp.first %}{{ class.name }} & {% else %}{{ class.name }}{% endif %}{% endfor %}{% elsif type_temp.size > 2 %}{% for class in type_temp %}{% if class == type_temp.first %}{{ class.name }}{% elsif class == type_temp.last %} & {{ class.name }}{% else %}, {{ class.name }}{% endif %}{% endfor %}{% else %}{% for class in type_temp %}{{ class.name }}{% endfor %}{% endif %} (In-Person)
     {% endif %}

     {% assign type_temp = section_temp | where: 'type', 'Online' %}
     {% if type_temp.size > 0 %}
       {% if count == 1 %} & {% endif %}
       {% if type_temp.size == 2 %}{% for class in type_temp %}{% if class == type_temp.first %}{{ class.name }} & {% else %}{{ class.name }}{% endif %}{% endfor %}{% elsif type_temp.size > 2 %}{% for class in type_temp %}{% if class == type_temp.first %}{{ class.name }}{% elsif class == type_temp.last %} & {{ class.name }}{% else %}, {{ class.name }}{% endif %}{% endfor %}{% else %}{% for class in type_temp %}{{ class.name }}{% endfor %}{% endif %} (Online)
     {% endif %} Instructor: {{ instructor.name }}</b><br>
     Email: <b><a href="mailto:{{ instructor.email }}">{{ instructor.email }}</a></b>
     {% assign count = 0 %}
   </li>

{% endfor %}
</ul>

## Course Webpages
* <b>Main Public Website</b><br>
  <a href="https://go.illinois.edu/stat100">go.illinois.edu/stat100</a> -- You can also google "stat 100" :)
* <b>LON-CAPA Site</b><br>
  <a href="http://www.lon-capa.illinois.edu/" target="_blank">http://www.lon-capa.illinois.edu/</a><br>
  All homework and bonus work are submitted and graded immediately on Lon Capa.
* <b>Canvas Site</b><br>
  <a href="http://canvas.illinois.edu/" target = "_blank">http://canvas.illinois.edu/</a><br>
  We're using Canvas to post announcements, lecture videos, and display grades.
  <!-- * <b><a href="{{ site.data.info.course-link1 }}" target="\_blank">{{ site.data.info.course-link1 }}</a></b>
    <br>You can also google "stat 100" :) -->

## Course Materials
* **Required Workbook: {{ site.data.info.textbook.name }} by {{ site.data.info.textbook.authors}}. {{ site.data.info.textbook.edition }}.**
    1. Available at the Illini Union Bookstore for {{ site.data.info.textbook.price }} or online at **<a href="https://buy.stipes.com/products/uiuc-stat-100-sp23" target="_blank">Stipes</a>**.
    2. This notebook is the only thing that's required to purchase for Stat 100!
    3. You will use this notebook each week during class!<br>
* **Required Calculator:** You'll also need a calculator for exams. Any calculator that can do basic operations and square roots will be fine. I recommend <b><a href="{{ site.data.info.calculator }}" target="\_blank">this one!</a></b> 
* **Optional iClicker for In Person class only:** I will be doing iClicker questions for extra credit in the in person class each day. Online class- do not by an iClicker, you’ll get extra credit in other ways!

## Class Times
All students are either enrolled in the in person section of Stat 100 OR the online version.  Details are found here:
<ul>
{% for class in site.data.info.sections %}
  <li>
    <b>{{ class.type }} Section {{ class.name }}:</b> {{ class.times }} {{ class.location }}
  </li>
{% endfor %}
</ul>

## Office Hours
* <b>{{ site.short-title }} Office Hours</b> will be offered each week {{ site.data.info.office-hours.days }} from {{ site.data.info.office-hours.times }} in the {{ site.data.info.office-hours.location }}
* We also have online office hours Monday and Wednesday evenings from 8-10pm on zoom! 
* Feel free to stop by anytime for help. Karle and the Stat 100 CAs will be there to answer any questions you may have about the course, assignments, or anything you need. If you are unavailable during these times and want to meet, send us an email at <a href="mailto:{{ site.data.info.main-email }}">{{ site.data.info.main-email }}</a> and we will set up a time!

## Technical Issues
* If you experience a glitch in Lon Capa/Canvas, first, try logging out and logging back in. If this doesn't work, send an email to {{ site.data.info.technical.name }} <b><a href="mailto:{{ site.data.info.technical.email }}">{{ site.data.info.technical.email }}</a></b> describing the problem. Please make sure to include a screenshot of the error in your e-mail. You can also stop by office hours and get help in person!

## Homework Schedule
* Homework is due {{ site.data.info.hw-duedates }} (see <b><a href="{{ site.baseurl }}/pages/calendar.html">calendar</a></b>) on <b><a href="http://www.lon-capa.illinois.edu/" target="\_blank">Lon-Capa</a></b>. You can ask questions on the Lon Capa discussion boards or stop by office hours any time to get homework help!
* <b style="color:red;">We do NOT accept late hw, but we do drop your 3 lowest HW scores. This means you can miss 3 HW assignments without any penalty!</b>
* There are many ways to get help so don’t hesitate to ask!  Also, please do not ask for an extension.  To be fair to everyone, extension requests will not be granted since you can miss 3 assignments without penalty.  If something happens where you will miss more than 3 HW assignments, please contact your instructor right away and we will work something out!

## Exam Schedule
* There will be 3 evening exams and a cumulative final. See the <b><a href="{{ site.baseurl }}/pages/exam_schedule.html">Exam Schedule</a></b> for dates, times, and locations.
  * <b>Exam 1:</b> {{ site.data.info.exams[0].date }} from 7-8:30pm
  * <b>Exam 2:</b> {{ site.data.info.exams[1].date }} from 7-8:30pm
  * <b>Exam 3:</b> {{ site.data.info.exams[2].date }} from 7-8:30pm
  * <b>Final for In Person Section L2:</b> Friday May 12th from 1:30-4:30pm
  * <b>Final for Online Section O1:</b> Tuesday May 9th from 1:30-4:30pm

* For Exams 1-3, there will be a main conflict at 4:30pm on exam days!  You will be able to sign up for these on Lon Capa the week before.  All exams for both the in person and online sections will be in person.  If you are not on the UIUC campus, please contact us immediately to set something up.

## Grade for Required Work

* **Grade for required work**
  1. 3 Exams: 60% (each worth 20%)
  2. Homework: 15%
  3. Final Exam: 25%

**Overall Grade is Translated into a Letter Grade as follows:**

{% include grade.html %}

## Bonus Work
**Bonus Points — You may earn between 0 and 100 Bonus Points.**
**Everyone may earn between 0 and 100 Bonus Points.** Every bonus point earned helps your overall grade, but even if you do no bonus work, you can still get 100% for the course. In other words, bonus points can only help you.  Bonus points are extra credit. Here’s how you can get them:
  1. **Pre-Lecture bonus points (23 bonus points)**<br>
  Each class there will be a short pre-lecture video posted on Lon Capa followed by a few questions. The pre-lectures are designed to give you a preview of the basic concepts you’ll see in the actual lectures. There are 23 prelectures and each is worth 1 bonus point.

  2. **Lon Capa Surveys (25 bonus points)**<br>
  There will be 5 surveys due on the first Friday of each month (see the course calendar). Each survey is worth 5 bonus points. The surveys are all anonymous. Lon Capa just records whether or not you submitted a survey, not who submitted which answer. You must answer every question on the survey to get the 5 points.

  3. **iClicker Points (in person class only, 22 bonus points)**<br>
  There are 44 classes this semester and each class is worth 0.5 bonus points.  You get the 0.5 point per class period if you answer all of the iClicker questions for that day.

  4. **Notebook Submission (30 points for the in person class, 52 points for the online classes)**<br>
  We will look over your notebook at the final.  You’ll get full credit if you have all of the pages from lecture filled in.  You may skip all of the practice exams and summary pages.  If you’re missing more than 3 required pages, don’t bother to turn in the notebook because you will receive negative bonus points.  You will pick up the notebook at the end of the semester to keep forever.

  5. **Research Opportunities**<br>
  There are usually a few research opportunities to participate in throughout the semester. The details will be posted on our course Canvas page as they come up! These opportunities are completely optional but give those who want to a chance to participate in a real study going on at the University.

**How do these bonus points get calculated into your grade?**  At the end of the semester, take your total bonus points (capped at 100) and divide them by 20. This will be how many percentage points get added to your grade! For example, if you have all 100 bonus points, you’d take 100 and divide it by 20 to get 5. So, if you have an 80% (B-) in the class, the bonus will bring you up to an 85% (B).  You may have more than 100 bonus points, but the max that will count will be 100.

## Course Outline
* **Experimental Design**: observational studies vs. randomized experiments, why randomized controls are key, confounders in observational studies, Simpson's Paradox, intent to treat analysis, etc.
* **Descriptive Statistics**: mean, median, SD, histograms, box plots, etc.
* **The Normal Approximation**: normal curve, etc.
* **Linear Regression**: correlation coefficient, simple linear regression, the RMSE, etc.
* **Probability**: chance, multiplication rule, addition rule, conditional probability, Bayes rule, etc.
* **Statistics for Random Variables**: expected value and standard error of chance processes, probability histograms and the Central Limit Theorem, developing simple chance models box models that more complicated sampling processes can be translated into, the Law of Averages, etc.
* **Sampling and Statistical Inference**: using sample means and percents to estimate population means and proportions, attaching margins of errors to our estimates by computing confidence intervals, why randomized sampling is key, etc.
* **Significance Tests**: one sample and two sample z-tests, t-tests, and chi-square tests for goodness of fit and independence, the focus is on understanding how these tests depend on chance models.
* **Limits of Significance Tests**: understanding what the p-value means and under what circumstances it is valid (for example, hypotheses must be stated before looking at the data, the total number of experiments before significant results were found must be reported, etc.)

## Academic Integrity
* If you cheat on an exam or attempt to cheat on an exam in this class you’re very likely to get caught and the consequences will be <b>SEVERE</b>. See the <b><a href="https://studentcode.illinois.edu/" target="\_blank">University Student Code of Conduct</a></b>.
* You are not allowed to work with other people on exams and you are not allowed to use cheating websites like Chegg. All exams will be in person.  We have multiple versions of all exams that may look identical at first glance but are not. Bottom line is, please don’t cheat. It’s not worth risking your entire college career and you will get caught. If you are caught, you will get a 0 on the exam and be reported to the university.

## DRES Accommodations
* I am happy to offer accommodations for disabilities verified through DRES (<b><a href="http://www.disability.illinois.edu/" target="\_blank">http://www.disability.illinois.edu/</a></b>). Please email me a copy of your letter during Week 1. I will provide the extra time accommodation for any student who needs it and sends me their DRES letter.  If you have any other questions or need any other accommodations, don’t hesitate to reach out. <a href="{{ site.data.info.rickroll }}">&#128522;</a>
