{% assign skills = site.data.data.skills %}
{% if skills %}

<section class="resume-section" id="skills">
<h2 style="text-align: center; margin-bottom:20px;">Skills</h2>
  <div class="container">
    <!-- Core from main-hub identity/blocks.yml expertise.core; change the hub first. -->
    <div class="row">
      <div class="col">
        <div class="serviceBox">
          <h3 class="title">{{skills.core.title}}</h3>
          <p class="description" style="color:black">{{skills.core.text}}</p>
        </div>
      </div>
    </div>
    <div class="row">
      {% for g in skills.groups %}
      <!---------------------------------------------------------------------------------->
      <div class="col-md">
        <div class="serviceBox">
          <h3 class="title">{{g.name}}</h3>
          {% for l in g.items %}
            <a href="#" onclick="return false;" class="read-more  sub_skill">{{l}}</a>
          {% endfor %}
          <h3 class="title"></h3>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>
{% endif %}
