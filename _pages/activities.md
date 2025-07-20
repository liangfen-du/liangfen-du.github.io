---
layout: archive
title: "Activities"
permalink: /activities/
author_profile: true
---

<ul class="activity-list">
  {% for activity in site.data.activities %}
  <li class="activity-item">
    <div class="activity-image">
      {% for image in activity.images %}
        <img src="{{ image.src }}" alt="{{ image.alt }}" style="{{ image.style }}">
      {% endfor %}
    </div>
    <div class="activity-text">
      {{ activity.date }}: {{ activity.description }}
    </div>
  </li>
  {% endfor %}
</ul>

<!-- You can add content here using markdown or HTML -->

<!-- Example:
### Conference Presentations
*   **Event Name 1**, *Location*, Date - "Title of Presentation"
*   **Workshop Name 1**, *Location*, Date - "Topic"

### Invited Talks
*   **Institution Name**, *Location*, Date - "Title of Talk"
-->
