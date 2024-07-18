---
layout: page
permalink: /things i can do/
title: Things I Can Do
description: Integer eu ante ornare amet commetus vestibulum blandit integer in curae ac faucibus integer non. Adipiscing cubilia elementum integer lorem ipsum dolor sit amet.
nav: true
nav_order: 4
---



<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
 
    {% include repository/repo_user.liquid username=user %}

</div>

---
## GitHub users

{% if site.data.repositories.github_users %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---


{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

## GitHub Repositories

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
