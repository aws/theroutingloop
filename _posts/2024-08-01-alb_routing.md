---
layout: default
title:  "AWS Application Load Balancer - Routing Algorithms and Health Checking"
videoid: oRz4Ln1zOLg
date:   2024-08-01 10:30:00 -0800
abstract: "In this session, we'll explore the routing algorithms of AWS Application Load Balancer, including round robin, least outstanding request, and weighted random, to efficiently manage and distribute traffic. We'll also cover the configuration and importance of health checking to ensure that only healthy instances receive traffic. "
hosts: "Alex Huides, Tom Adamski"
guests: ""
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