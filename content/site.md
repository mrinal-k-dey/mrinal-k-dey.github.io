# Site settings
<!--
  name / footer = top bar and footer text on every page.

  SECTIONS = the pages in the menu, in this order.
  Each "## Section" block needs:
    id      = short name, used in the web address (…/#publications)
    label   = text shown in the menu
    layout  = how the page looks. Built-in layouts:
                home, education, research, publications, contact  (custom designs)
                gallery, list, text                                     (general-purpose)
    folder  = folder inside content/ that holds this page's content.md + files
    nav     = optional, "no" hides it from the menu (page still reachable by link)

  TO ADD A NEW PAGE (e.g. a photo gallery):
    1. Copy content/_templates/gallery  ->  content/gallery
    2. Put your photos in content/gallery and list them in its content.md
    3. Add a "## Section" block below with layout: gallery, folder: gallery
  Nothing else needs to change.
-->

name: Mrinal Kanti Dey
footer: © 2026 Mrinal Kanti Dey

## Section
id: home
label: Home
layout: home
folder: home

## Section
id: education
label: Education
layout: education
folder: education

## Section
id: research
label: Research
layout: research
folder: research

## Section
id: publications
label: Publications
layout: publications
folder: publications

## Section
id: contact
label: Contact
layout: contact
folder: contact
