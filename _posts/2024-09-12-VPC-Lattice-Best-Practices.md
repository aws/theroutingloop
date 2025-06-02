---
layout: default
title:  "Amazon VPC Lattice - Best Practices, Migrations, and How it all Works"
videoid: CWGWLydrSKE
date:   2024-09-12 10:30:00 -0800
abstract: "Join Jamie and Matt as we talk to Justin Davies the Principal Product Manager of Amazon VPC Lattice. We will talk about best practices, where Lattice fits in this new crazy world of networking, and how to migrate to Lattice. We will also talk about how things work under the hood to give a better picture on what is going on with your packets! Bring your questions!"
hosts: "Jamie and Matt"
guests: "Justin Davies, Principal Product Manager EC2N"
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