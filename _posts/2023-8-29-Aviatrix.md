---
layout: default
title:  "AWS and Aviatrix - A chat about AWS Cloud Wan and all things cloud connectivity"
videoid: 
date:   2024-08-29 10:30:00 -0800
abstract: "Join us to learn more about the AWS Cloud WAN Connector in partnership with Aviatrix. <br> <br> The AWS Cloud WAN Connector facilitates automatic integration of Aviatrix transit gateways with AWS Cloud WAN, allowing users to extend their AWS-centric operations to a multi-cloud strategy effortlessly. <br> <br> In this session, we’ll demonstrate how this solution automates the provisioning of transit gateways, the creation of network domains, and the establishment of BGP over GRE connections to Cloud WAN hubs, ensuring consistent network segmentation across environments. <br> <br> By leveraging event-driven automation and running on the Aviatrix Extensibility Framework, the connector streamlines network management, reduces manual intervention, and enhances operational efficiency for organizations using AWS as their primary cloud. <br> We’ll also discuss how using the new CloudWAN Service Insertion integration, customers can now achieve centralized east-west and internet-egress inspection, secure multi-cloud connectivity, encrypt on-premises connectivity end-to-end, secure connectivity to AWS partitions such as AWS China and AWS GovCloud, and provide B2B connectivity with partners."
hosts: "Jamie, Matt, and Shridhar"
guests: "Christopher McHenry, VP of Product at Aviatrix"
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
      <iframe src="https://player.twitch.tv/?video={{ page.videoid }}&parent=www.theroutingloop.net&parent=127.0.0.1&autoplay=false" height="315" width="560" allowfullscreen="" frameborder="0"></iframe>
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