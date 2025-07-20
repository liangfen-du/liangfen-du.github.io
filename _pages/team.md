---
layout: archive
# title: "Team"
permalink: /team/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<div class="team-container">

  <!-- Postdoctoral Researchers -->
  <h1>Postdoctoral Researchers</h1>
  {% for member in site.data.team.postdocs %}
    <div class="team-member">
      <div class="team-member-image">
        <img src="{{ member.image }}" alt="{{ member.name }}">
      </div>
      <div class="team-member-info">
        <h2>{{ member.name }}</h2>
        <h3>{{ member.title }}</h3>
        <p>Research topics: {{ member.research }}</p>
        <table>
          {% for edu in member.education %}
          <tr>
            <td><strong>{{ edu.degree }}</strong></td>
            <td>{{ edu.university }}</td>
          </tr>
          {% endfor %}
        </table>
        <div class="team-member-contact">
          {% for contact in member.contact %}
            <a href="{{ contact.url }}" {% if contact.type != 'email' %}target="_blank"{% endif %}><i class="{% if contact.type == 'email' %}fas fa-envelope{% else %}ai ai-researchgate{% endif %}"></i> {{ contact.type | capitalize }}
            </a>
          {% endfor %}
        </div>
      </div>
    </div>
  {% endfor %}

  <!-- PhD Students -->
  <h1>PhD Students</h1>
  {% for member in site.data.team.phd_students %}
    <div class="team-member">
      <div class="team-member-image">
        <img src="{{ member.image }}" alt="{{ member.name }}">
      </div>
      <div class="team-member-info">
        <h2>{{ member.name }}</h2>
        <h3>{{ member.title }}</h3>
        <p>Research topics: {{ member.research }}</p>
        <table>
          {% for edu in member.education %}
          <tr>
            <td><strong>{{ edu.degree }}</strong></td>
            <td>{{ edu.university }}</td>
          </tr>
          {% endfor %}
        </table>
        <div class="team-member-contact">
          {% for contact in member.contact %}
            <a href="{{ contact.url }}" {% if contact.type != 'email' %}target="_blank"{% endif %}><i class="{% if contact.type == 'email' %}fas fa-envelope{% else %}ai ai-researchgate{% endif %}"></i> {{ contact.type | capitalize }}
            </a>
          {% endfor %}
        </div>
      </div>
    </div>
  {% endfor %}

  <!-- Alumni -->
  <h1>Alumni</h1>
  {% for member in site.data.team.alumni %}
    <div class="team-member">
      <div class="team-member-image">
        <img src="{{ member.image }}" alt="{{ member.name }}">
      </div>
      <div class="team-member-info">
        <h2>{{ member.name }}</h2>
        <h3>{{ member.title }}</h3>
        <p>Research topics:</p>
        <ul>
          {% for topic in member.research_topics %}
          <li>{{ topic }}</li>
          {% endfor %}
        </ul>
        <table>
          {% for edu in member.education %}
          <tr>
            <td><strong>{{ edu.degree }}</strong></td>
            <td>{{ edu.university }}</td>
          </tr>
          {% endfor %}
        </table>
        <div class="team-member-contact">
          {% for contact in member.contact %}
            <a href="{{ contact.url }}" target="_blank">
              <i class="{% case contact.type %}{% when 'email' %}fas fa-envelope{% when 'researchgate' %}ai ai-researchgate{% when 'googlescholar' %}ai ai-google-scholar{% when 'linkedin' %}fab fa-linkedin{% endcase %}"></i> 
              {{ contact.type | capitalize }}
            </a>
          {% endfor %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>

