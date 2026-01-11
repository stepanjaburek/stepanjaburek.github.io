---
title: "Publications"
type: landing
date: 2024-05-19

design:
  spacing: '6rem'

# Page sections
sections:
  - block: collection
    content:
      title: "Published Work"
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: citation
      template: citation
      show_date: false
      show_summary: false
      show_image: false
  - block: collection
    content:
      title: "Work in Progress"
      text: ""
      filters:
        folders:
          - publications
        exclude_featured: true
    design:
      view: citation
      template: citation
      show_date: false
      show_summary: false
      show_image: false
---
