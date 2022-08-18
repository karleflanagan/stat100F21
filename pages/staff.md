---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
{% include landing_small.html title='About Us' %}

<div id="about" class="offset" style="margin-top: 5px;">
  <div class="bg-light py-4">
    <div class="container py-4">
      <div class="col-12 text-center">
        <div class="text-center" style="margin-bottom: 3em;">
          <h2 class="display-5 font-weight-light">Course Staff</h2>
        </div>
        <p class="lead text-left" style="font-size: 1.15em;">{{ site.data.staff.about }}</p>
      </div>
      <div class="row text-center">



        {% include staff_cards.html role='Instructor' seniority='1' %}
        {% include staff_cards.html role='Instructor' seniority='S19' %}
        {% include staff_cards.html role='Course Assistant' seniority='S19' %}
        {% include staff_cards.html role='Course Assistant' seniority='F19' %}
        {% include staff_cards.html role='Course Assistant' seniority='F20' %}
        {% include staff_cards.html role='Course Assistant' seniority='F21' %}
        {% include staff_cards.html role='Course Assistant' seniority='S22' %}
      </div>
    </div>
  </div>
</div>
