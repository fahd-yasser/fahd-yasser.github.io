---
permalink: /
title: "Bio"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a second year PhD Student in Computer Vision at the University of Bristol supervised by Dr. Michael Wray. My research focuses on investigating sources and impacts of biases in vision-language models. Prior to starting my PhD, I worked for four years as a Machine Learning Engineer, developing business-critical systems for chatbots, Opical Character Recognition (OCR), and document understanding.

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

# Publications

<div class="publications-scroll-container">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    <div class="publication-item">
      <div class="publication-content">
        {% if pub.figure %}
        <div class="publication-figure">
          <img src="{{ pub.figure }}" alt="Publication Figure for {{ pub.title }}" class="pub-image">
        </div>
        {% endif %}
        
        <div class="publication-details">
          <p class="publication-entry">
            {{ pub.title }}
          </p>
          
          {% if pub.citation %}
          <p class="publication-citation">
            {{ pub.citation }}
          </p>
          {% endif %}
          
          <div class="publication-links">
            {% if pub.paper_link %}
            <a href="{{ pub.paper_link }}" target="_blank" class="paper-link">Paper</a>
            {% endif %}
            
            {% if pub.website %}
            <a href="{{ pub.website }}" target="_blank" class="website-link">Project Website</a>
            {% endif %}
            
            {% if pub.doi %}
            <a href="https://doi.org/{{ pub.doi }}" target="_blank" class="doi-link">DOI</a>
            {% endif %}
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<style>
.publications-scroll-container {
  max-height: 500px; /* Increased height to accommodate larger figures */
  overflow-y: auto;
  border: none; /* Remove border */
  padding: 10px;
  background-color: var(--background-primary);
  margin-top: 15px;
  color: var(--text-primary);
  font-size: 0.85em;
}

.publication-item {
  margin-bottom: 15px;
  border-bottom: none; /* Remove bottom border */
  padding-bottom: 10px;
}

.publication-content {
  display: flex;
  align-items: stretch; /* Ensure equal height */
  }

.publication-figure {
  margin-right: 15px;
  flex-shrink: 0;
  display: flex;
  align-items: center; /* Vertically center the image */
  justify-content: center; /* Horizontally center the image */
  }

.pub-image {
  max-width: 250px; /* Maintained figure size */
  max-height: 150px; /* Limit height to match citation section */
  width: auto;
  height: auto;
  max-height: 150px;
  /* object-fit: contain; Preserve aspect ratio */
  }

.publication-details {
  display: flex;
  flex-direction: column;
  justify-content: center; /* Vertically center text */
  }

.publication-citation {
  margin: 0 0 10px 0;
  font-size: 0.75em;
  color: var(--text-secondary);
  line-height: 1.4;
  }

.publication-links {
  display: flex;
  gap: 10px;
  margin-top: 10px;
}

.publication-links a {
  color: var(--link-color);
  text-decoration: none;
  font-weight: bold;
  font-size: 0.8em;
  padding: 3px 8px;
  border: 1px solid var(--link-color);
  border-radius: 4px;
  transition: all 0.3s ease;
}

.publication-links a:hover {
  color: var(--link-hover-color);
  border-color: var(--link-hover-color);
  background-color: rgba(0,102,204,0.1);
}

.publication-entry {
  margin: 0 0 10px 0;
  line-height: 1.4;
  font-size: 0.8em;
}

.publication-entry a {
  color: var(--link-color);
  text-decoration: none;
  font-weight: bold;
  font-size: 1.2em !important; /* Force larger size */
  font-weight: 900 !important; /* Force extra bold */
}

.publication-entry a:hover {
  color: var(--link-hover-color);
  text-decoration: underline;
}

.publication-entry strong {
  margin-right: 8px;
  color: var(--text-secondary);
  font-size: 1em;
}

</style>