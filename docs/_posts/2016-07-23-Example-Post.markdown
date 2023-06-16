---
layout: post
title:  "Sample Post"
date:   2016-07-23 13:01:16 -0700
categories: personal
description: A short bit of text that will appear below the link to this page in the post list.
permalink: /example/
carousels:
  - images:
    - image: /assets/images/tree.png
    - image: /assets/images/water1.png
    - image: /assets/images/water2.png
---
This page is an example of how to use the includes.
## images
There are 2 ways to embed images shown below
### inline
{% include image.html url="/assets/images/tree.png" caption="Trees in hope" %}
### carousel
to do this include the images in the header above
{% include carousel.html height="500" unit="px" number="1" %}
## pdfs
you can embed pdfs from an external site or internal depending on how you program it. if displaying multiple pdfs on a single page make sure to assign them different ID's
### internal
{% include pdf.html id="pdf" url="/assets/pdfs/pdf.pdf" %}
### external
{% include pdf.html id="pdf1" external="true" url="https://github.com/ealexanderca/website-repo/raw/main/docs/assets/pdfs/pdf.pdf" %}
## stls
you can embed them using this command and change orientation
### internal
{% include stl.html url="/assets/3dfiles/cvt.stl" %}
### external
{% include stl.html external="true" url="https://github.com/ealexanderca/website-repo/raw/main/docs/assets/3dfiles/cvt.stl" %}
## videos
currently I only use youtube to embed videos because it is the easiest method to upload and host large video files
{% include youtube.html ID="RS5kh3pxKJU" %}
