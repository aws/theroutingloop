---
layout: default
title:  "Amazon VPC and dynamic routing with VPC Route Server"
videoid: jdj-EnTVYMA
date:   2025-10-22 11:00:00 -0800
abstract: "Join us as we explore how AWS Route Server brings dynamic routing to Amazon VPC. See how it enables BGP route exchange between your virtual appliances and AWS networking services, making it easier to build scalable, automated, and flexible cloud networks."
hosts: "Jamie Wenzel"
guests: "Ammar Latif, Pr. Solutions Architect, Telco, AWS "
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
