---
layout: page
title: Projects
permalink: /projects.html
---

<div class="project-card" markdown="1">

## 🎬 AI Script-to-Video Agent <span class="status status-wip">In Progress</span>

An AI agent that turns a written script into a finished video, end to end:

1. **Script analysis** — extract themes, keywords, and named entities with spaCy
2. **Stock footage search** — query the Pexels API with the extracted keywords
3. **Clip selection & assembly** — score, download, and stitch the best clips into a coherent video

The script-analysis and footage-search stages are working; clip scoring and
video assembly are up next.

<p class="tags">
  <span class="tag">Python</span>
  <span class="tag">spaCy</span>
  <span class="tag">Pexels API</span>
  <span class="tag">NLP</span>
  <span class="tag">Colab</span>
</p>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/toufiq171/toufiq.github.io/blob/main/notebooks/ai-video-agent.ipynb)

</div>

<div class="project-card" markdown="1">

## 🛰️ Text-to-Image with FLUX.1 <span class="status status-done">Complete</span>

Generating images from text prompts with the **FLUX.1-dev** diffusion model
through the Hugging Face Inference API (Together AI provider) — for example,
*"an artificial satellite orbiting a neutron star, with heavy radiation
shielding."* Includes saving generated images straight to Google Drive.

<p class="tags">
  <span class="tag">FLUX.1-dev</span>
  <span class="tag">Hugging Face</span>
  <span class="tag">Diffusion Models</span>
  <span class="tag">Colab</span>
</p>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/toufiq171/toufiq.github.io/blob/main/notebooks/ai-video-agent.ipynb)

</div>

<div class="project-card" markdown="1">

## 🔎 Script Keyword Extraction <span class="status status-done">Complete</span>

The NLP engine behind the video agent, useful on its own: feed it any text
and it pulls out the nouns, verbs, and named entities that best describe the
scene — ready to use as search queries, tags, or summaries. Built with spaCy's
`en_core_web_sm` pipeline using part-of-speech tagging and named-entity
recognition.

<p class="tags">
  <span class="tag">Python</span>
  <span class="tag">spaCy</span>
  <span class="tag">NER</span>
  <span class="tag">POS Tagging</span>
</p>

</div>

<div class="project-card" markdown="1">

## 🌐 This Website <span class="status status-live">Live</span>

The site you're reading — a Jekyll static site with hand-rolled CSS
animations (animated gradient hero, scroll-reveal sections, hover-lift
cards), built and deployed automatically to GitHub Pages by GitHub Actions
on every push. Respects `prefers-reduced-motion` for accessibility.

<p class="tags">
  <span class="tag">Jekyll</span>
  <span class="tag">CSS Animations</span>
  <span class="tag">GitHub Actions</span>
  <span class="tag">GitHub Pages</span>
</p>

[View source on GitHub →](https://github.com/toufiq171/toufiq.github.io)

</div>
