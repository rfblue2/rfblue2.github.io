---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects">
    <h1>Projects</h1>
    
    <div class="project-list">
        {% for project in site.data.projects %}
        <article class="project">
            <h2>
                <a href="{{ project.link }}" target="_blank" rel="noopener noreferrer">
                    {{ project.name }}
                </a>
            </h2>
            
            <div class="project-meta">
                <time datetime="{{ project.date }}">{{ project.date | date: "%B %Y" }}</time>
            </div>
            
            <p class="project-description">{{ project.description }}</p>
            
            <div class="project-technologies">
                {% for tech in project.technologies %}
                <span class="tech-tag">{{ tech }}</span>
                {% endfor %}
            </div>
        </article>
        {% endfor %}
    </div>
</div> 