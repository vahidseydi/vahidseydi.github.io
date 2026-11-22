{% assign CTs = site.data.data.teaching %}
{% if CTs %}

<section class="resume-section" id="teaching">
<h2 style="text-align: center; margin-bottom:20px;">Teaching</h2>
  <div class="container">
    <div class="row" >
        {% for CT in CTs %}
          <!---------------------------------------------------------------------------------->
          <div class="col-md">
            <div class="serviceBox">
                <h3 class="title">{{CT.institution}}</h3>
                <a href="#" onclick="return false;" class="read-more  date" style="float:left">{{CT.start}}</a><a href="#" onclick="return false;" class="read-more  date" style="float:right">{{CT.end}}</a>
                </br></br></br>
                {% for g in CT.groups %}
                  {% if g.name %}<p style="text-align:left; color:black; font-weight:bold">{{g.name}}</p>{% endif %}
                  {% for l in g.courses %}
                    <p style="text-align:left; color:gray">{{l}}</p>
                  {% endfor %}
                {% endfor %}
                <h3 class="title"></h3>
            </div>
          </div>
          <!---------------------------------------------------------------------------------->
        {% endfor %}
    </div>
  </div>
</section>
{% endif %}
