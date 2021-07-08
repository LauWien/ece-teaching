# Overview of the teaching & learning material by the ECE program

Copyright (c) 2021 IIASA; ![License](https://img.shields.io/github/license/iiasa/ece-teaching)

This is a [Sphinx](http://sphinx-doc.org/) project for the documentation of the 
build of the teaching and learning website by the Energy, Climate, and 
Environment Program (ECE). The website can be found [here](https://teaching.ece.iiasa.ac.at/).

The MIT license applies only to this site and not to the teaching and learning
content.

## Scope & Aim

This repository contains pages with relevant information about teaching events, 
including links to relevant websites and the teaching material (e.g., pdf, pptx, 
recorded videos). Any such material should not be committed to this repository, 
but be stored in an appropriate location such as the IIASA publication 
[repository](pure.iiasa.ac.at) or a folder on ldom002.

The material comprises workshops organized by ECE, university courses taught
by ECE staff, tutorials, etc.

## Instructions

### How to install dependencies and build locally
1. Install dependencies and start 
[Sphinx](https://www.sphinx-doc.org/en/master/usage/quickstart.html)

      `pip install -r requirements.txt`
      
      `$ sphinx-quickstart`

2. Build from the command line. On Linux or macOS:

    `make html`

   On Windows:

    `.\make html`
 
 3. Open the rendered html page to see if everything fits:
 
    `_build/html/index.html`

### How to add new content

1. Fork the repository. 

2. Create a new branch.

3. Update 

	a) either the existing ReST file `index.rst` or, 

	b) implement your ReST file on the top level and link it within the `index.rst`
	(this creates a sub-page). 

Implementing a subpage (b)) is only recommended if your materials covers series 
of lectures, including video tutorial(s) and multiple other files. 

4. Create a PR to the main branch of 
[iiasa/ece-teaching](https://github.com/iiasa/ece-teaching/) with yourself 
as an assignee and a reviewer.

### How to write

Use the following references for writing your ReST file:

- [Quick reStructuredText](http://docutils.sourceforge.net/docs/user/rst/quickref.html) 
reference from docutils.
- [ReST cheat sheet](https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html) 
by Thomas Cokelaer.
- [Sphinx](http://www.sphinx-doc.org/) documentation, including reference on 
Sphinx-specific ReST syntax.

See the following example on how to link e.g. your video from the IIASA
publication [repository](pure.iiasa.ac.at) or a folder on ldom002.

```
.. raw:: html

	<video width="640" height="360" controls preload="none" controlsList="nodownload">
		<source src="Your file path" type="video/mp4">
 ```
