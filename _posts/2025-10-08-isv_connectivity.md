---
layout: default
title:  "Modern Connectivity Patterns for ISVs on AWS"
videoid: USEsGM3aFTY
date:   2025-10-08 11:00:00 -0800
abstract: "How do Independent Software Vendors build secure, scalable connectivity with their customers on AWS? In this session, we’ll unpack common networking patterns ISVs use to expose their applications to end customers — and how they gain access to customer-owned data sources in the reverse direction. We’ll compare public connectivity approaches with private networking options, from VPC peering and Transit Gateway to application-centric services like AWS PrivateLink and Amazon VPC Lattice."
hosts: "Alexandra Huides, Tom Adamski"
guests: ""
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
