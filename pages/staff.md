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

        <div class="col-xl-12 col-sm-12 mb-1">
          <div class="staff-card bg-white rounded shadow-sm py-2 px-0">
            <a href="{{ site.data.info.rickroll }}">
              <img src="{{ site.baseurl }}/assets/img/staff-photos/stat100_impact_final1.png" class="img-fluid mb-2 img-thumbnail shadow-sm" style="width=100%;">
            </a>
            <h5 class="mb-0">Meet the STAT 100 Team!:)</h5>
            <h6 class="mb-0">Come meet us at STAT 100 <a href="{{ site.data.info.office-hours.link }}">Zoom</a> Office Hours!:)</h6>
          </div>
        </div>

        {% include staff_cards.html role='Lead Instructor' seniority='1' %}
        {% include staff_cards.html role='Course Assistant' seniority='2' %}
        {% include staff_cards.html role='Course Assistant' seniority='3' %}
        {% include staff_cards.html role='Course Assistant' seniority='4' %}
      </div>
    </div>
  </div>
</div>
