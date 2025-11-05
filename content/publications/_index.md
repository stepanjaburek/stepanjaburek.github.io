---
title: "Publications"
type: landing
date: 2024-05-19

design:
  spacing: '5rem'

# Page sections
sections:
  - block: collection
    content:
      title: "Published Work"
      text: "Selected peer-reviewed and published papers."
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
      text: "Ongoing projects and drafts in development."
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
