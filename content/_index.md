---
title: ''
type: landing

design:
  spacing: '6rem'

sections:
  # BLOQUE 1: Portada con tu foto y botón
  - block: resume-biography-3
    content:
      username: admin
      text: |
        Estudiante de Ingeniería en Software en UABC, apasionado por la programación, el desarrollo web y la investigación. En este portafolio encontrarás mis prácticas, proyectos y materiales del curso Paradigmas de la Programación.
      button:
        text: Ver Prácticas
        url: /post/
      headings:
        about: Sobre mí
        education: UABC
        interests: Intereses
    design:
      css_class: hbx-bg-gradient
      avatar:
        size: medium
        shape: circle

  # BLOQUE 2: Texto corto de presentación
  - block: markdown
    content:
      title: '📚 Prácticas y portafolio'
      text: |-
        Aquí encontrarás mis prácticas y reportes del curso **Paradigmas de la Programación**:
        - Programación en C, Python y Haskell  
        - Desarrollo web, análisis y migración de sistemas  
        - Experimentos y documentación académica
    design:
      columns: '1'

  # BLOQUE 3: Últimas prácticas tipo blog
  - block: collection
    id: blog
    content:
      title: Últimas Prácticas
      page_type: post
      count: 6
      filters:
        folders:
          - post
    design:
      view: article-grid
      columns: 3
      spacing:
        padding: [0, 0, 0, 0]
      show_image: true
---
