---
layout: default
title: "Matthew Moisseyev"
---

<div class="row">
    <div class="col-md-8">
        <h1 class="page-title">
            <img class="profile-img-small d-md-none" src="{{ '/assets/profile.jpg' | relative_url }}" alt="Matthew Moisseyev" />
            Matthew Moisseyev
        </h1>
        <div class="social-links">
            <a href="mailto:mmoisseyev2@unl.edu" title="Email"><i class="fas fa-envelope"></i></a>
            <a href="https://www.linkedin.com/in/matthew-moisseyev" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
            <a href="https://github.com/mmoiss" title="GitHub"><i class="fab fa-github"></i></a>
        </div>
        <section id="about" class="mt-4">
            <!-- <h2 class="section-title">About</h2> -->
            {% capture bio %}{% include bio.md %}{% endcapture %}
            <div class="bio-content">
                {{ bio | markdownify }}
            </div>
        </section>
    </div>
    <div class="col-md-4">
        <img class="profile-img d-none d-md-block" src="{{ '/assets/profile.jpg' | relative_url }}" alt="Matthew Moisseyev" />
    </div>
</div>

{% assign sorted_publications = site.publications | sort:"date" %}
{% assign selected_publications = sorted_publications | where:"selected", true %}

<section id="hackathons" class="mt-5">
    <h2 class="section-title"><b>Hackathons</b></h2>
    <div class="hackathons-list">
        {% assign sorted_hackathons = site.hackathons | sort: "order" %}
        {% for project in sorted_hackathons %}
            {% include project_item.html %}
        {% endfor %}
    </div>
</section>

<!-- 
<section id="publications" class="mt-5">
    <h2 class="section-title">Research</h2>
    <div class="publications-list">
        {% for publication in selected_publications reversed %}
            {% include publication_item.html %}
        {% endfor %}
        {% for publication in sorted_publications reversed %}
            {% unless publication.selected %}
                {% include publication_item.html %}
            {% endunless %}
        {% endfor %}
    </div>
</section>
-->

