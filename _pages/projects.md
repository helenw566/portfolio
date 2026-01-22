---
permalink: /projects/
title: "Projects"
author_profile: true
---

## Projects & Research

<style>
.publications-list {
  margin: 2rem 0;
}

.publication-item {
  background: white;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  overflow: hidden;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  border: 1px solid #e1e5e9;
  margin-bottom: 1rem;
}

.publication-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(0,0,0,0.12);
}

.publication-header {
  display: flex;
  align-items: center;
  min-height: 100px;
  gap: 0;
}

.publication-thumbnail {
  width: 200px;
  height: 120px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 2rem;
  font-weight: bold;
  position: relative;
  flex-shrink: 0;
  overflow: hidden;
  line-height: 0;
  margin-top: 0;
}

.publication-thumbnail img {
  max-width: 100%;
  max-height: 100%;
  width: auto;
  height: auto;
  object-fit: contain;
  display: block;
  margin: auto;
}

.publication-image {
  transition: transform 0.3s ease;
}

.publication-thumbnail:hover .publication-image {
  transform: scale(1.05);
}

.publication-initial {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 2rem;
  font-weight: bold;
}

.publication-content {
  flex: 1;
  padding: 1rem 1.5rem 1rem 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.publication-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #2c3e50;
  margin: 0 0 0.3rem 0;
  line-height: 1.3;
}

.publication-authors {
  font-size: 0.9rem;
  color: #555;
  margin-bottom: 0.3rem;
  line-height: 1.3;
}

.publication-authors strong {
  color: #667eea;
  font-weight: 700;
}

.publication-venue {
  font-size: 0.85rem;
  color: #e74c3c;
  font-weight: 500;
  margin-bottom: 0.5rem;
}

.publication-excerpt {
  font-size: 0.85rem;
  color: #666;
  line-height: 1.4;
  margin-bottom: 0.75rem;
  flex: 1;
}

.publication-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: auto;
}

.publication-link {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0.3rem 0.6rem;
  background: #f8f9fa;
  border: 1px solid #e9ecef;
  border-radius: 6px;
  text-decoration: none;
  color: #495057;
  font-size: 0.75rem;
  font-weight: 500;
  transition: all 0.2s ease;
}

.publication-link:hover {
  background: #e9ecef;
  color: #212529;
  text-decoration: none;
}

.publication-link.primary {
  background: #667eea;
  color: white;
  border-color: #667eea;
}

.publication-link.primary:hover {
  background: #5a6fd8;
  color: white;
}

.publication-link.secondary {
  background: #28a745;
  color: white;
  border-color: #28a745;
}

.publication-link.secondary:hover {
  background: #218838;
  color: white;
}

.publication-link.tertiary {
  background: #ffc107;
  color: #212529;
  border-color: #ffc107;
}

.publication-link.tertiary:hover {
  background: #e0a800;
  color: #212529;
}



@media (max-width: 768px) {
  .publication-header {
    flex-direction: column;
  }
  
  .publication-thumbnail {
    width: 100%;
    height: 120px;
  }
  
  .publication-thumbnail::before {
    font-size: 1.5rem;
  }
}
</style>

<div class="publications-list">
{% for post in site.projects reversed %}
  <div class="publication-item">
    <div class="publication-header">
      <div class="publication-thumbnail">
        {% if post.image %}
          <img src="{{ site.baseurl }}/assets/images/{{ post.image }}" alt="{{ post.title }}" class="publication-image">
        {% else %}
          <div class="publication-initial">{{ post.title | slice: 0, 1 }}</div>
        {% endif %}
      </div>
      <div class="publication-content">
        <div>
          <h3 class="publication-title">{{ post.title }}</h3>
          {% if post.authors %}
          <div class="publication-authors">{{ post.authors | replace: 'Yi Ru Wang', '<strong>Yi Ru Wang</strong>' | replace: 'Wang, Y. R.', '<strong>Wang, Y. R.</strong>' }}</div>
          {% endif %}
          {% if post.venue %}
          <div class="publication-venue">{{ post.venue }}</div>
          {% endif %}
          {% if post.excerpt %}
          <div class="publication-excerpt">{{ post.excerpt }}</div>
          {% endif %}
        </div>
        <div class="publication-links">
          {% if post.paperurl %}
          <a href="{{ post.paperurl }}" class="publication-link primary" target="_blank">
            📄 Paper
          </a>
          {% endif %}
          {% if post.website %}
          <a href="{{ post.website }}" class="publication-link secondary" target="_blank">
            🌐 Website
          </a>
          {% endif %}
          {% if post.code %}
          <a href="{{ post.code }}" class="publication-link tertiary" target="_blank">
            💻 Code
          </a>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
{% endfor %}
</div>
