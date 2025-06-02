---
layout: default
title:  "How to migrate to Amazon VPC Lattice and use DNS to simplify service discovery"
videoid: QFMHA-HkEp4
date:   2024-10-17 10:30:00 -0800
abstract: "This session is an in-depth exploration of migrating to Amazon VPC Lattice. We will whiteboard DNS migration options, do a live demo of a new automated DNS configuration solution for VPC Lattice, and answer questions. The goal is to help you understand how you can leverage VPC Lattice to simplify service discovery and ease the migration process for clients and applications."
hosts: "Alexandra Huides"
guests: "Pablo Sánchez Carmona, Sr. Solutions Architect, Networking <br> Scott Morrison, Sr. Solutions Architect, Networking <br> Maialen Loinaz Anton, Solutions Architect " 

---
<div class="content-area">
  <span class="date">{{ page.date | date: "%-d %B %Y" }}</span>

  <h1>{{ page.title }}</h1>

  <p><b>Hosts:</b><br>{{ page.hosts }}</p>
  <p><b>Guests:</b><br>{{ page.guests }}</p>
  <div class="abstract">
    <b>Abstract:</b><br>{{ page.abstract }}
  </div>

  {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
  {% capture posttime %}{{page.date | date: '%s'}}{% endcapture %}
  {% if posttime < nowunix %}   
    <div class="video-container">
      <iframe 
        src="https://www.youtube.com/embed/{{ page.videoid }}?autoplay=0" 
        height="315" 
        width="560" 
        allowfullscreen 
        frameborder="0">
    </iframe>
    </div>
    <a href="https://pulse.aws/survey/6ONETCNV" class="button">Session Feedback/Content Suggestions</a>
  {% else %}
    <p>Session hasn't started. Join live on <b>{{ page.date | date: "%-d %B %Y" }} at 10:30AM PST / 1:30PM EST / 6:30PM GMT</b></p>
    <div class="video-container">
      <iframe src="https://player.twitch.tv/?channel=aws&parent=www.theroutingloop.net&parent=127.0.0.1&autoplay=false" height="315" width="560" allowfullscreen="" frameborder="0"></iframe>
    </div>
  {% endif %}

  {% if page.videoid == null %}
    <b>Video on demand will become available soon after the livestream</b>
  {% endif %}
</div>