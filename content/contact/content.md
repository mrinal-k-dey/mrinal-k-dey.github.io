# Contact
<!--
  formEndpoint = web address of your Google Sheet log (see FORM-SETUP.md).
                 Leave empty and the form tells visitors to use email instead.
  Each "## Link" block is used on BOTH the Home card and the Contact page.
    label = short text (Home)   long = longer text (Contact page)
    url   = web / mailto link   file = a file in this folder (e.g. cv.pdf, downloads)
    preview = optional page shown in a pop-up before downloading (used for the CV)
    icon  = SVG in icons/ (single-colour; it gets tinted with "color")
  The CV file itself lives in content/cv/cv.pdf.
-->

label: GET IN TOUCH
title: Contact
email: mrinal.k.dey@iitb.ac.in
formEndpoint: https://script.google.com/macros/s/AKfycbzFjV3UiTbUd5zaM1Z4in3PXKRATQM9CtMIRJSXo3UXN4RLwGCSXmMZRyIbikJQR1Q/exec

## Link
label: Email
long: mrinal.k.dey@iitb.ac.in
url: mailto:mrinal.k.dey@iitb.ac.in
icon: icons/email.svg
color: oklch(0.52 0.15 25)

## Link
label: LinkedIn
long: LinkedIn
url: https://www.linkedin.com/in/mrinal-kanti-dey-4a685b15b/
icon: icons/linkedin.svg
color: oklch(0.5 0.13 245)

## Link
label: Scholar
long: Google Scholar
url: https://scholar.google.com/citations?hl=en&user=c0cYZTwAAAAJ
icon: icons/scholar.svg
color: oklch(0.52 0.13 155)

## Link
label: CV
long: Download CV
file: ../cv/cv.pdf
preview: ../../CV.dc.html
icon: icons/cv.svg
color: oklch(0.52 0.14 300)
