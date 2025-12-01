---
layout: page
title: "Red Wing Models"
permalink: /en/models/
lang: en
lang_ref: models-index
description: "Browse all Red Wing boot models available at Chez Gerry 1958 in Canada."
---

<section class="section">
  <div class="container">
    <h1>Red Wing models available</h1>
    <p>
      Here is a selection of Red Wing boots offered at
      <a href="https://chezgerry1958.com" target="_blank" rel="noopener">Chez Gerry 1958</a>.
      Click a model to view detailed specs and purchase links.
    </p>

    <div class="model-grid">
      {% assign en_models = site.models | where: "lang", "en" | sort: "title" %}
      {% for model in en_models %}
        <article class="model-card">
          <h2 class="model-card-title">
            <a href="{{ model.url | relative_url }}">{{ model.title }}</a>
          </h2>

          {% if model.description %}
            <p class="model-card-desc">
              {{ model.description }}
            </p>
          {% endif %}

          <p class="model-card-link">
            <a href="{{ model.url | relative_url }}">View details →</a>
          </p>
        </article>
      {% endfor %}
    </div>
  </div>
</section>
