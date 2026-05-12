---
title: Research
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

<div style="display: flex; gap: 10px; justify-content: center; margin-bottom: 30px; flex-wrap: wrap;">
  <a href="#journal" class="button" style="margin: 0;">{% include icon.html icon="fa-solid fa-book-open" %} Journal Papers</a>
  <a href="#conference" class="button" style="margin: 0;">{% include icon.html icon="fa-solid fa-users" %} Conference Papers</a>
</div>

{% include search-box.html %}

<div class="tags" style="justify-content: center; margin-top: 15px; margin-bottom: 30px;">
  <a href="?search=%22tag:+medical-imaging%22" class="tag" style="background: var(--light-gray);">Medical Imaging</a>
  <a href="?search=%22tag:+fMRI%22" class="tag" style="background: var(--light-gray);">fMRI</a>
  <a href="?search=%22tag:+XAI%22" class="tag" style="background: var(--light-gray);">XAI</a>
  <a href="?search=%22tag:+autism%22" class="tag" style="background: var(--light-gray);">Autism</a>
  <a href="?search=%22tag:+generative-AI%22" class="tag" style="background: var(--light-gray);">Generative AI</a>
</div>

{% include search-info.html %}

{% include section.html %}

<h2 id="journal">Journal</h2>

{% include list.html data="citations" component="citation" style="rich" filter="publisher and (publisher.include?('Transactions') or publisher.include?('NeuroImage') or publisher.include?('Scientific Reports') or publisher.include?('Psychiatry Research'))" %}

{% include section.html %}

<h2 id="conference">Conference</h2>

{% include list.html data="citations" component="citation" style="rich" filter="publisher and (publisher.include?('Lecture Notes') or publisher.include?('Proceedings') or publisher.include?('Conference'))" %}
