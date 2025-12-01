---
layout: page
title: "Modèles Red Wing"
permalink: /models/
lang: fr
lang_ref: models-index
description: "Découvrez tous les modèles de bottes Red Wing disponibles chez Chez Gerry 1958 au Canada."
---

<section class="section">
  <div class="container">
    <h1>Modèles Red Wing disponibles</h1>
    <p>
      Voici une sélection de bottes Red Wing offertes chez
      <a href="https://chezgerry1958.com" target="_blank" rel="noopener">Chez Gerry 1958</a>.
      Cliquez sur un modèle pour voir la fiche détaillée, les caractéristiques et le lien d’achat.
    </p>

    <div class="model-grid">
      {% assign fr_models = site.models | where: "lang", "fr" | sort: "title" %}
      {% for model in fr_models %}
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
            <a href="{{ model.url | relative_url }}">Voir la fiche →</a>
          </p>
        </article>
      {% endfor %}
    </div>
  </div>
</section>
