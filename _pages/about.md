---
permalink: /
title: "Bio"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a second year PhD Student in Computer Vision at the University of Bristol supervised by Dr. Michael Wray. My research focuses on investigating sources and impact biases in vision-language models. Prior to starting my PhD, I worked for four years as a Machine Learning Engineer, developing business-critical systems for chatbots, Opical Character Recognition (OCR), and document understanding.

# News

<div class="news-scroll-container">
  {% assign sorted_news = site.news | sort: 'date' | reverse | slice: 0, 5 %}
  {% for post in sorted_news %}
    <div class="news-item">
      <p class="news-entry">
        <strong>{{ post.date | date: "%b %d, %Y" }}</strong> 
        {{ post.content | markdownify }}
      </p>
    </div>
  {% endfor %}
</div>

<style>
:root {
  --link-color: #0066cc;
  --link-hover-color: #004080;
  --link-visited-color: #800080;
}

[data-theme="dark"] {
  --link-color: #4da6ff;
  --link-hover-color: #80c1ff;
  --link-visited-color: #cc80ff;
}

.news-scroll-container {
  max-height: 250px; /* Slightly reduced height */
  overflow-y: auto;
  border: 1px solid var(--border-color);
  padding: 10px; /* Reduced padding */
  background-color: var(--background-primary);
  margin-top: 15px;
  color: var(--text-primary);
  font-size: 0.85em; /* Reduce overall font size */
}

.news-item {
  margin-bottom: 8px; /* Reduced margin */
}

.news-entry {
  margin: 0;
  line-height: 1.4; /* Tighter line height */
  font-size: 0.8em; /* Even smaller font size */
}

.news-entry strong {
  margin-right: 8px; /* Slightly reduced margin */
  color: var(--text-secondary);
  font-size: 0.9em; /* Slightly smaller date */
}

.news-entry a {
  color: var(--link-color);
  text-decoration: none;
  font-weight: bold;
  font-size: 0.9em; /* Smaller link text */
  transition: color 0.3s ease;
}

.news-entry a:hover {
  color: var(--link-hover-color);
  text-decoration: underline;
}

.news-entry a:visited {
  color: var(--link-visited-color);
}
</style>