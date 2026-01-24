---
permalink: /projects/
title: "Projects"
---

<style>

/* list objects */
.projects-list {
  display: grid;
  grid-template-columns: 1fr; 
  gap: 1rem;
  margin: 2rem 0;
}

.research-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr); 
  gap: 1rem;
  margin: 2rem 0;
}

/* project item  */
.project-item {
  background: white;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  overflow: hidden;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  border: 1px solid #e1e5e9;
  margin-bottom: 1rem;
  box-sizing: border-box;
}

.project-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(0,0,0,0.12);
}

.project-header {
  display: flex;
  align-items: center;
  min-height: 100px;
  gap: 0;
}

.project-thumbnail {
  width: 200px;
  height: 200px;
  background: #f8f9fa;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  flex-shrink: 0;
  overflow: hidden;
  line-height: 0;
  margin-top: 0;
}

.project-thumbnail img {
  max-width: 100%;
  max-height: 100%;
  width: auto;
  height: auto;
  object-fit: contain;
  display: block;
  margin: auto;
}

.project-image {
  transition: transform 0.3s ease;
}

.project-thumbnail:hover .project-image {
  transform: scale(1.05);
}

.project-initial {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #13724c;
  font-size: 4rem;
  font-weight: bold;
}

.project-content {
  flex: 1;
  padding: 1rem 1.5rem 1rem 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.project-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #2c3e50;
  margin: 0 0 0.3rem 0;
  line-height: 1.3;
}

.project-authors {
  font-size: 0.8rem;
  color: #555;
  margin-bottom: 0.3rem;
  line-height: 1.3;
  font-style: italic;
}

.project-authors strong {
  color: #131313;
  font-weight: 700;
}

.project-venue {
  font-size: 0.85rem;
  color: #338cd5;
  font-weight: 500;
  margin-bottom: 0.5rem;
}

.project-excerpt {
  font-size: 0.85rem;
  color: #666;
  line-height: 1.4;
  margin-bottom: 0.75rem;
  flex: 1;
}

.project-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: auto;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0.3rem 0.6rem;
  border: 1px solid;
  border-radius: 6px;
  text-decoration: none;
  font-size: 0.75rem;
  font-weight: 500;
  transition: all 0.2s ease;
}

.project-link.primary {
  background: white;
  color: #212529;
  border-color: #0abc84b2;
}

.project-link.primary:hover {
  background: #0abc845a;
  color: #212529;
}

.project-link.secondary {
  background: white;
  color: #212529;
  border-color: #7f28a1b2;
}

.project-link.secondary:hover {
  background: #7f28a155;
  color: #212529;
}

.project-link.tertiary {
  background: white;
  color: #212529;
  border-color: #0a6cbcb2;
}

.project-link.tertiary:hover {
  background: #0a6cbc5c;
  color: #212529;
}


@media (max-width: 768px) {
  .project-header {
    flex-direction: column;
  }
  
  .project-thumbnail {
    width: 100%;
    height: 120px;
  }
  
  .project-thumbnail::before {
    font-size: 1.5rem;
  }
}


/* research item  */
.research-item {
  background: white;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  overflow: hidden;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  border: 1px solid #e1e5e9;
  margin-bottom: 1rem;
  box-sizing: border-box;
}

.research-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(0,0,0,0.12);
}

.research-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: auto;
  gap: 1rem;
}

.research-thumbnail {
  width: auto;
  height: auto;
  background: #f8f9fa;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  flex-shrink: 0;
  overflow: hidden;
  line-height: 0;
  margin-top: 0;
}

.research-thumbnail img {
  max-width: 100%;
  max-height: 100%;
  width: auto;
  height: auto;
  object-fit: contain;
  display: block;
  margin: 1rem;
}

.research-image {
  transition: transform 0.3s ease;
}

.research-thumbnail:hover .research-image {
  transform: scale(1.05);
}

.research-initial {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #13724c;
  font-size: 4rem;
  font-weight: bold;
}

.research-content {
  flex: 1;
  padding: 0.5rem 1.5rem 1rem 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.research-title {
  font-size: 0.85rem;
  font-weight: 600;
  color: #2c3e50;
  margin: 0 0 0.1rem 0;
  line-height: 1.3;
}

.research-venue {
  font-size: 0.7rem;
  color: #338cd5;
  font-weight: 500;
  margin-bottom: 0.5rem;
  margin-top: 0.5rem;
}

.research-excerpt {
  font-size: 0.65rem;
  color: #666;
  line-height: 1.4;
  margin-bottom: 0.75rem;
  flex: 1;
}

.research-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-top: auto;
}

.research-link {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0.3rem 0.6rem;
  border: 1px solid;
  border-radius: 6px;
  text-decoration: none;
  font-size: 0.75rem;
  font-weight: 500;
  transition: all 0.2s ease;
}

.research-link.primary {
  background: white;
  color: #212529;
  border-color: #0abc84b2;
}

.research-link.primary:hover {
  background: #0abc845a;
  color: #212529;
}

.research-link.secondary {
  background: white;
  color: #212529;
  border-color: #7f28a1b2;
}

.research-link.secondary:hover {
  background: #7f28a155;
  color: #212529;
}

.research-link.tertiary {
  background: white;
  color: #212529;
  border-color: #0a6cbcb2;
}

.research-link.tertiary:hover {
  background: #0a6cbc5c;
  color: #212529;
}


@media (max-width: 768px) {
  .research-header {
    flex-direction: column;
  }
  
  .research-thumbnail {
    width: 100%;
    height: 120px;
  }
  
  .research-thumbnail::before {
    font-size: 1.5rem;
  }
}

</style>

<p>
Here is a selection of my computational work, including my
<a href="#thesis">undergraduate thesis</a>,
<a href="#publications">academic publications</a>,
<a href="#projects">data science projects</a>,
<a href="#research">research</a>, 
and personal ventures.
</p>

<h2 id="thesis">Thesis</h2>

<div class="projects-list">
{% for post in site.thesis %}
  <div class="project-item">
    <div class="project-header">
      <div class="project-thumbnail">
        {% if post.image %}
          <img src="{{ site.baseurl }}/assets/images/{{ post.image }}" alt="{{ post.title }}" class="project-image">
        {% else %}
          <div class="project-initial">{{ post.title | slice: 0, 1 }}</div>
        {% endif %}
      </div>
      <div class="project-content">
        <div>
          <h3 class="project-title">{{ post.title }}</h3>
          {% if post.authors %}
          <div class="project-authors">{{ post.authors | replace: 'Helen Wang,', '<strong>Helen Wang</strong>'}}</div>
          {% endif %}
          {% if post.venue %}
          <div class="project-venue">{{ post.venue }}</div>
          {% endif %}
          {% if post.excerpt %}
          <div class="project-excerpt">{{ post.excerpt }}</div>
          {% endif %}
        </div>
        <div class="project-links">
          {% if post.paperurl %}
          <a href="{{ site.baseurl }}{{ post.paperurl }}" class="project-link primary" target="_blank">
            📄 Paper
          </a>
          {% endif %}
          {% if post.website %}
          <a href="{{ post.website }}" class="project-link secondary" target="_blank">
            🌐 Media
          </a>
          {% endif %}
          {% if post.code %}
          <a href="{{ post.code }}" class="project-link tertiary" target="_blank">
            💻 Code
          </a>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
{% endfor %}
</div>

<h2 id="publications">Publications</h2>

<div class="projects-list">
{% for post in site.papers %}
  <div class="project-item">
    <div class="project-header">
      <div class="project-thumbnail">
        {% if post.image %}
          <img src="{{ site.baseurl }}/assets/images/{{ post.image }}" alt="{{ post.title }}" class="project-image">
        {% else %}
          <div class="project-initial">{{ post.title | slice: 0, 1 }}</div>
        {% endif %}
      </div>
      <div class="project-content">
        <div>
          <h3 class="project-title">{{ post.title }}</h3>
          {% if post.authors %}
          <div class="project-authors">{{ post.authors | replace: 'Helen Wang,', '<strong>Helen Wang</strong>,'}}</div>
          {% endif %}
          {% if post.venue %}
          <div class="project-venue">{{ post.venue }}</div>
          {% endif %}
          {% if post.excerpt %}
          <div class="project-excerpt">{{ post.excerpt }}</div>
          {% endif %}
        </div>
        <div class="project-links">
          {% if post.paperurl %}
          <a href="{{ post.paperurl }}" class="project-link primary" target="_blank">
            📄 Paper
          </a>
          {% endif %}
          {% if post.website %}
          <a href="{{ post.website }}" class="project-link secondary" target="_blank">
            🌐 Media
          </a>
          {% endif %}
          {% if post.code %}
          <a href="{{ post.code }}" class="project-link tertiary" target="_blank">
            💻 Code
          </a>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
{% endfor %}
</div>

<h2 id="projects">Data Science Projects</h2>

<div class="projects-list">
{% for post in site.projects %}
  <div class="project-item">
    <div class="project-header">
      <div class="project-thumbnail">
        {% if post.image %}
          <img src="{{ site.baseurl }}/assets/images/{{ post.image }}" alt="{{ post.title }}" class="project-image">
        {% else %}
          <div class="project-initial">{{ post.title | slice: 0, 1 }}</div>
        {% endif %}
      </div>
      <div class="project-content">
        <div>
          <h3 class="project-title">{{ post.title }}</h3>
          {% if post.authors %}
          <div class="project-authors">{{ post.authors | replace: 'Helen Wang,', '<strong>Helen Wang</strong>,'}}</div>
          {% endif %}
          {% if post.venue %}
          <div class="project-venue">{{ post.venue }}</div>
          {% endif %}
          {% if post.excerpt %}
          <div class="project-excerpt">{{ post.excerpt }}</div>
          {% endif %}
        </div>
        <div class="project-links">
          {% if post.paperurl %}
          <a href="{{ post.paperurl }}" class="project-link primary" target="_blank">
            📄 Paper
          </a>
          {% endif %}
          {% if post.website %}
          <a href="{{ post.website }}" class="project-link secondary" target="_blank">
            🌐 Dashboard
          </a>
          {% endif %}
          {% if post.code %}
          <a href="{{ post.code }}" class="project-link tertiary" target="_blank">
            💻 Code
          </a>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
{% endfor %}
</div>

<h2 id="research">Research</h2>

<div class="research-list">
{% for post in site.research %}
  <div class="research-item">
    <div class="research-header">
      <div class="research-thumbnail">
        {% if post.image %}
          <img src="{{ site.baseurl }}{{ post.image }}" alt="{{ post.title }}" class="research-image">
        {% else %}
          <div class="research-initial">{{ post.title | slice: 0, 1 }}</div>
        {% endif %}
      </div>
      <div class="research-content">
        <div>
          <h3 class="research-title">{{ post.title }}</h3>
          {% if post.venue %}
          <div class="research-venue">{{ post.venue }}</div>
          {% endif %}
          {% if post.excerpt %}
          <div class="research-excerpt">{{ post.excerpt }}</div>
          {% endif %}
        </div>
        <div class="research-links">
          {% if post.paperurl %}
          <a href="{{ site.baseurl }}{{ post.paperurl }}" class="research-link primary" target="_blank">
            🏆 Poster
          </a>
          {% endif %}
          {% if post.website %}
          <a href="{{ post.website }}" class="research-link secondary" target="_blank">
            🌐 Media
          </a>
          {% endif %}
          {% if post.code %}
          <a href="{{ post.code }}" class="research-link tertiary" target="_blank">
            💻 Code
          </a>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
{% endfor %}
</div>