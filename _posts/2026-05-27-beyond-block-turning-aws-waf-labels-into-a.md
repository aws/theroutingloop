---
layout: post
title: 'Beyond Block: Turning AWS WAF Labels Into a Control Plane for Your Origin'
videoid: ''
date: 2026-05-27 11:00:00 -0800
abstract: 'AWS WAF labels gave us granular detection - Bot Control alone emits dozens - but acting on each combination used to mean a rule per outcome, and rule lists grew faster than detection improved. Dynamic label interpolation flips that: one rule resolves a label namespace at evaluation time and produces a value into a response body, response header, or request header to origin. In this session we walk through four live demos that compose into a real pattern - a WAF that doesn''t just block, but tells your block page why it fired, redirects challenged users with full context, forwards Bot Control signals to your origin without lookup tables, and drives CloudFront cache identity from custom labels signals. We''ll close with an aws-samples repo already using this pattern to serve different content to AI agents, heavy users, and humans from the same URL.'
hosts: 'Tom Adamski'
guests: 'Eitav Arditti, Sr. Specialist Solutions Architect, Edge'
---
