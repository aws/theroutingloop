---
layout: default
title:  "re:Invent 2024 - Chalk Talks - Centralized network traffic inspection: Key insights & lessons learned"
videoid: 
date:   2025-03-12 11:00:00 -0800
abstract: "Centralized network traffic inspection using AWS Transit Gateway or AWS Cloud WAN and AWS Network Firewall or Gateway Load Balancer is a common architecture adopted by many customers. This architecture has many benefits both in terms of operations and cost efficiencies. In this chalk talk, explore the advantages of centralized inspection and learn valuable lessons from AWS experiences working with customers to plan and execute this architecture successfully."
hosts: "Jamie Wenzel"
guests: "Joe Flanagan, Senior Solutions Architect, Networking <br> Mehdi Dahane, Solutions Architect, Networking"
---
{% assign event_date = page.date | date: "%Y%m%d" %}

{% capture ics_content %}
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//Your Website//Event Calendar//EN
BEGIN:VEVENT
UID:{{ page.title | replace: " ", "-" }}@yourwebsite.com
DTSTAMP:{{ "now" | date: "%Y%m%dT%H%M%SZ" }}
DTSTART;TZID=America/Los_Angeles:{{ event_date }}T110000
DTEND;TZID=America/Los_Angeles:{{ event_date }}T120000
SUMMARY:{{ page.title }}
DESCRIPTION:{{ page.abstract | strip_html }}
LOCATION:Online
END:VEVENT
END:VCALENDAR
{% endcapture %}

{% assign ics_filename = page.title | replace: " ", "-" | replace: ":", "" | downcase %}

<div class="content-area">
  <span class="date">{{ page.date | date: "%-d %B %Y" }}</span>

  <h1>{{ page.title }}</h1>

  <p><b>Hosts:</b><br>{{ page.hosts }}</p>
  <p><b>Guests:</b><br>{{ page.guests }}</p>
  <p>
    📅 <a href="data:text/calendar;charset=utf8,{{ ics_content | uri_escape }}" 
          download="{{ ics_filename }}.ics">
          Add to Calendar
       </a>
  </p>
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
    <p>Session hasn't started. Join live on <b>{{ page.date | date: "%-d %B %Y" }} at 11 AM PT / 2 PM ET / 7 PM UK</b></p>
    <div class="video-container">
      <iframe src="https://player.twitch.tv/?channel=aws&parent=www.theroutingloop.net&parent=127.0.0.1&autoplay=false" height="315" width="560" allowfullscreen="" frameborder="0"></iframe>
    </div>
  {% endif %}

  {% if page.videoid == null %}
    <b>Video on demand will become available soon after the livestream</b>
  {% endif %}
</div>
