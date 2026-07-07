---
layout: post
title: "Building an AI Script-to-Video Agent"
date: 2026-07-07
categories: ai projects
---

Can an AI agent turn a written script into a finished video, all by itself?
That's the experiment I've been running in a Colab notebook, and this post
walks through how the pipeline works so far.

## The idea

Given a short script — say, a noir scene about a detective chasing a stolen
diamond through foggy London — the agent should:

1. **Understand the script**: pick out the themes, objects, actions, and mood
2. **Find matching footage**: search free stock-video platforms for clips
3. **Assemble the video**: pick the best clips, trim them, and stitch them together

## Step 1: Script analysis with spaCy

The first stage uses spaCy's `en_core_web_sm` pipeline. After processing the
script, I extract two kinds of signals:

- **Named entities** — places and things like *London* or *the British Museum*
- **Content words** — nouns and verbs (lemmatized, stop-words removed), like
  *detective*, *raven*, *search*, *mystery*

For my test script this produced keywords like `detective`, `London`,
`diamond`, `fog`, and `mystery` — exactly the sort of terms you'd type into
a stock footage search yourself.

## Step 2: Stock footage search with the Pexels API

The keywords become search queries against the
[Pexels video API](https://www.pexels.com/api/). For each result the agent
records the duration, resolution, and a direct download link for the highest
quality MP4. Searching *"Eye of Ra British Eye London Museum"* returned
drone shots of the Thames, the London Eye, and Big Ben — remarkably on-theme
for an automated pipeline.

A couple of practical notes:

- Keep the API key in Colab's **Secrets** tab, never in the notebook itself
- Respect rate limits — Pexels' free tier is generous but not unlimited

## What's next

The remaining stages are clip **scoring** (which clip best matches which
sentence?), **preprocessing** (resize and trim to a common format), and
**assembly** with a video editing library like MoviePy. I'm also curious
whether embedding-based matching (CLIP similarity between script sentences
and video thumbnails) beats plain keyword search.

Try the notebook yourself:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/toufiq171/toufiq.github.io/blob/main/notebooks/ai-video-agent.ipynb)
