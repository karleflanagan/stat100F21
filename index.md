---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults


layout: default
---

<!-- landing photo page -->
{% include landing.html image='/assets/img/stat100desk.jpg' %}

/assets/img/stat100desk.jpg

<!-- Start of Sections Section -->
<div id="sections" class="offset" style="margin-top:5px;">
  <div class="jumbotron" style="background-color: white;">
    <!-- title -->
    <div class="col-12 narrow text-center">
      <h1 style="padding-bottom: 20px; text-transform: uppercase;">{{ site.title }} {{ site.semester }} Sections</h1>
      <div class="heading-underline"></div>
    </div>
    <div class="row text-center">
    <!-- loops through section information -->
      <!-- <div class="col-md-6">
        <div class="feature">
          <i class="{{ site.data.info.in-person-icon }}" data-fa-transform="shrinks-5 up-4"></i>
          <h3>In Person Section: {% assign in_person = site.data.info.sections | where: 'type', 'In Person' %}{% if in_person.size == 2 %}{% for class in in_person %}{% if class == in_person.first %}{{ class.name }} & {% else %}{{ class.name }}{% endif %}{% endfor %}{% elsif in_person.size > 2 %}{% for class in in_person %}{% if class == in_person.first %}{{ class.name }}{% elsif class == in_person.last %} & {{ class.name }}{% else %}, {{ class.name }}{% endif %}{% endfor %}{% else %}{% for class in in_person %}{{ class.name }}{% endfor %}{% endif %}</h3>
          <p>{% for class in in_person %}
          <b>{{ class.name }} Instructor: {{ class.instructor }}</b><br>
          {{ class.times }} {{ class.location }}<br>
          {% endfor %}</p>
        </div>
      </div> -->
      <div class="col-md-12">
        <div class="feature">
          <a href="{{ site.data.info.rickroll }}"><i class="{{ site.data.info.online-icon }}" data-fa-transform="shrinks-5 up-4"></i></a>
          <h3>Online Section: {% assign online = site.data.info.sections | where: 'type', 'Online' %}{% if online.size == 2 %}{% for class in online %}{% if class == online.first %}{{ class.name }} & {% else %}{{ class.name }}{% endif %}{% endfor %}{% elsif online.size > 2 %}{% for class in online %}{% if class == online.first %}{{ class.name }}{% elsif class == online.last %} & {{ class.name }}{% else %}, {{ class.name }}{% endif %}{% endfor %}{% else %}{% for class in online %}{{ class.name }}{% endfor %}{% endif %}</h3>
          <p>{% for class in online %}
          <b>{{ class.name }} Instructor: {{ class.instructor }}</b><br>
          {{ class.times }}<br>{{ class.location }}<br>
          {% endfor %}</p>
        </div>
      </div>
    </div>
  </div>
</div>
<!-- End of Sections Section -->

<!-- Start of Links -->
<div id="links" class="offset">
  <!-- Class links section -->
  <div class="fixed-background">
    <div class="row dark text-center">
      <div class="col-12 text-center">
        <h3 class="heading">Links</h3>
        <div class="heading-underline"></div>
      </div>
      <!-- Loops through links -->
      {% for link in site.data.info.links1 %}
        <div class="col-md-3">
          <h3>{{ link.title }}</h3>
          <a class="btn btn-secondary btn-md" href="{{ link.url }}" target="\_blank">{{ link.subtitle }}</a>
        </div>
      {% endfor %}
    </div>
    <!-- background image for class link section -->
    <div class="fixed-wrap">
      <div class="fixed" style="background-image: url('{{ site.baseurl }}/assets/img/stat100book.jpg');">
        <div class="layer">
        </div>
      </div>
    </div>
  </div>
  <!-- End class links section -->
  <!-- Data Programs section -->
  <div class="jumbotron">
    <div class="narrow text-center">
      <div class="col-12">
        <h3 class="heading">Data Programs</h3>
        <div class="heading-underline"></div>
      </div>
      <!-- loops through data program links -->
      <div class="row text-center">
        {% for link in site.data.info.links2 %}
          <div class="col-md-4">
            <h3>{{ link.title }}</h3>
            <a class="btn btn-secondary btn-md" href="{{ link.url }}" target="\_blank">
              <div class="feature">
                <i class="{{ link.icon }}"></i><i class="fas fa-chevron-circle-right fa-2x"></i>
              </div>
            </a>
          </div>
        {% endfor %}
      </div>
      <!-- appreciation for John Marden -->
      <div class="col-12">
        <cite>Our data program was created by Professor <a href="https://stat.illinois.edu/directory/profile/jimarden" target="\_blank">John Marden</a>.
Thanks for being an integral part of STAT 100 team!</cite>
      </div>
    </div>
  </div>
  <!-- End of data programs section -->
</div>
<!-- End of Links -->

<!-- Start of Goals -->
<div id="goals" class="offset">
  <div class="narrow text-center">
    <!-- heading -->
    <div class="col-12">
      <h3 class="heading">Goals & Philosophy</h3>
      <div class="heading-underline"></div>
    </div>
    <div class="row text-center">
    <!-- loops through goals -->
    {% for goal in site.data.info.goals %}
      <div class="col-md-6">
        <h4>{{ goal.title }}</h4>
        <div class="sub-heading-underline"></div>
        <p>{{ goal.body }}</p>
      </div>
    {% endfor %}  
    </div>
  </div>
</div>

<div class="fixed-background testimonials">
  <div class="row dark text-center">
    <div class="col-12 text-center">
      <h3 class="heading">Students tell us that after Stat 100 they:</h3>
      <div class="heading-underline"></div>
      <ul class="lead narrow" style="text-align: left;">
        {% for experience in site.data.info.experiences %}
          <li>
            <p>{{ experience.text }}</p>
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
  <div class="fixed-wrap">
    <div class="fixed" style="background-image: url('{{ site.baseurl }}/assets/img/stat100book.jpg');">
      <div class="layer">
      </div>
    </div>
  </div>
</div>
