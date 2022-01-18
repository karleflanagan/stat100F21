---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults


layout: default
---

<!-- landing photo page -->
{% include landing.html image='/assets/img/stat100desk.jpg' %}


<!-- Start of Sections Section -->
<div id="sections" class="offset" style="margin-top:5px;">
  <div class="jumbotron" style="padding-top: 5px;">
    <!-- title -->
    <!-- <div class="col-12">
      <h3 class="heading">Data Programs</h3>
      <div class="heading-underline"></div>
    </div> -->
    <div class="col-12 narrow text-center">
      <h2 style="heading padding-bottom: 10px; text-transform: uppercase; font-weight: bold;">{{ site.title }} {{ site.semester }} Sections</h2>
      <div class="heading-underline"></div>
    </div>
    <div class="row text-center">
    <!-- loops through section information -->
      {% assign sections = site.data.info.sections %}
      <!-- <h1>{{ sections.size | modulo: 2 }}</h1> -->
      <!-- How many sections there are, How to divide space -->
      {% case sections.size %}
        {% when 1 %}
          {% assign spacing = "col-md-12" %}
        {% when 2 %}
          {% assign spacing = "col-md-6" %}
        {% when 3 %}
          {% assign spacing = "col-md-4" %}
        {% else %}
          {% assign spacing = "col-md-3" %}
      {% endcase %}
      {% for section in sections %}
        {% if section.type == "In Person" or section.type == "Online" %}
          {% if section.type == "In Person" %}
            {% assign icon = site.data.info.in-person-icon %}
          {% else %}
            {% assign icon = site.data.info.online-icon %}
          {% endif %}
          <div class="{{ spacing }}">
            <div class="feature">
              <i class="{{ icon }}" data-fa-transform="shrinks-5 up-4"></i>
              <h3>{{ section.type }} Section {{ section.name }}</h3>
              <p><b>Instructor: {{ section.instructor }}</b><br>
              {{ section.times }}<br>
              {{ section.location }}</p>
            </div>
          </div>
        {% endif %}
      {% endfor %}
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
        <h2 class="heading">Links</h2>
        <div class="heading-underline"></div>
      </div>
      <!-- Loops through links -->
      {% for link in site.data.info.links1 %}
        <div class="col-md-4">
          <h3>{{ link.title }}</h3>
          <a class="btn btn-secondary btn-sm" href="{{ link.url }}" target="\_blank" style="margin: 10px;">{{ link.subtitle }}</a>
        </div>
      {% endfor %}
      <!-- <div class="jumbotron col-12"> -->
        <div class="heading-underline" style="width: 90%; margin-top: 35px; margin-bottom: 35px;"></div>
      <!-- </div> -->
      <!-- </div>
      <div class="row dark text-center"> -->
      <div class="col-12 text-center">
        <h2 class="heading">Data Programs</h2>
        <div class="heading-underline"></div>
      </div>
      <!-- Loops through links -->
      {% for link in site.data.info.links2 %}
        <div class="col-md-4">
          <h3>{{ link.title }}</h3>
          <a class="btn btn-secondary btn-sm" href="{{ link.url }}" target="\_blank">
            <div class="feature">
              <i class="{{ link.icon }}"></i><i class="fas fa-chevron-circle-right fa-2x"></i>
            </div>
          </a>
        </div>
      {% endfor %}
      <div class="col-12">
        <cite style="font-size: 18px;">Our data program was created by Professor <a href="https://stat.illinois.edu/directory/profile/jimarden" target="\_blank" style="color=#e84a27;">John Marden</a>.
  Thanks for being an integral part of STAT 100 team!</cite>
      </div>
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
  <!-- <div class="jumbotron" style="padding: 5;">
    <div class="narrow text-center" style="margin: 0 auto; padding: 0px;">
      <div class="col-12">
        <h2 class="heading">Data Programs</h2>
        <div class="heading-underline"></div>
      </div> -->
      <!-- loops through data program links -->
      <!-- <div class="row text-center">
        {% for link in site.data.info.links2 %}
          <div class="col-md-4">
            <h3>{{ link.title }}</h3>
            <a class="btn btn-secondary btn-sm" href="{{ link.url }}" target="\_blank">
              <div class="feature">
                <i class="{{ link.icon }}"></i><i class="fas fa-chevron-circle-right fa-2x"></i>
              </div>
            </a>
          </div>
        {% endfor %}
      </div> -->
      <!-- appreciation for John Marden -->
      <!-- <div class="col-12">
        <cite style="font-size: 1.1vw;">Our data program was created by Professor <a href="https://stat.illinois.edu/directory/profile/jimarden" target="\_blank">John Marden</a>.
Thanks for being an integral part of STAT 100 team!</cite>
      </div>
    </div>
  </div> -->

  <!-- End of data programs section -->
</div>
<!-- End of Links -->

<!-- <div class="jumbotron col-12">
  <div class="heading-underline" style="width: 90%;"></div>
</div> -->

<!-- Start of Goals -->
<div id="goals" class="offset">
  <div class="jumbotron"  style="padding: 5; padding-top: 30px; margin-top:5px;">
    <div class="narrow text-center" style="margin: 0 auto; padding: 0px;">
      <!-- heading -->
      <div class="col-12">
        <h2 class="heading">Goals & Philosophy</h2>
        <div class="heading-underline"></div>
      </div>
      <div class="row text-center">
      <!-- loops through goals -->
      {% for goal in site.data.info.goals %}
        <div class="col-md-6">
          <h3 style="font-size: 25px;">{{ goal.title }}</h3>
          <div class="sub-heading-underline"></div>
          <p>{{ goal.body }}</p>
        </div>
      {% endfor %}  
      </div>
    </div>
    <!--  -->
    <div class="heading-underline" style="width: 90%; margin-top: 30px; margin-bottom: 30px;"></div>
    <!--  -->
    <div class="col-12 text-center">
      <h2 class="heading">Students tell us that after Stat 100 they:</h2>
      <div class="heading-underline"></div>
      <ul class="lead narrow" style="text-align: left; margin-top: 0px;">
        {% for experience in site.data.info.experiences %}
          <li style="font-size: 18px;">
            <p>{{ experience.text }}</p>
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
</div>

<!-- <div class="fixed-background testimonials">
  <div class="row dark text-center" style="padding: 15;">
    <div class="col-12 text-center">
      <h2 class="heading" style="font-size: 2vw;">Students tell us that after Stat 100 they:</h2>
      <div class="heading-underline"></div>
      <ul class="lead narrow" style="text-align: left; margin-top: 0px;">
        {% for experience in site.data.info.experiences %}
          <li style="font-size: 1.1vw;">
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
</div> -->
