---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-users" %}Team

Meet the members of DAISY Lab.

{% include section.html %}

### Professor
{% include list.html data="members" component="portrait" filter="role == 'pi'" %}

{% include section.html %}

### PhD Students
{% include list.html data="members" component="portrait" filter="role == 'phd' and group != 'alum'" %}

### MS Students
{% include list.html data="members" component="portrait" filter="role == 'ms' and group != 'alum'" %}

### Undergraduate Students
{% include list.html data="members" component="portrait" filter="role == 'undergrad' and group != 'alum'" %}

{% include section.html %}

### Alumni
{% include list.html data="members" component="portrait" filter="group == 'alum'" %}
