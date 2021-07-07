# Overview of the teaching & learning material by the ECE program

Copyright (c) 2021 IIASA

![License](https://img.shields.io/github/license/iiasa/ece-teaching)

This is a [Sphinx](http://sphinx-doc.org/) project for the documentation of the build of the teaching and learning website by the Energy, Climate, and Environment Program (ECE). The website can be found [here](https://teaching.ece.iiasa.ac.at/).

## Scope & Aim

The scope and aim of the repository is to create a Sphinx documentation, which is the basis for the teaching and learning website. This repository should contain all docs, but not the data, of the teaching and learning material. 

## Instructions

### How to install dependencies and build locally
1. Install dependencies and start Sphinx [sphinx_rtd_theme](https://sphinx-rtd-theme.readthedocs.io/)

      `pip install -r requirements.txt`
      
      `$ sphinx-quickstart`

2. Build from the command line. On Linux or macOS:

    `make html`

   On Windows:

    `.\make html`
 
 3. Open the rendered html page to see if everything fits:
 
    `_build/html/index.html`

### How to add new material

To add new material, fork the repository and either update the existing ReST file `index.rst` or, if you want to build a subpage, implement your ReST file on the top level and link it within the `index.rst` file. 

Implementing a subpage is only recommended if your materials covers series of lectures, including video tutorial(s) and multiple other files. 

### How to write

Use the following references for writing your ReST file:

- [Quick reStructuredText](http://docutils.sourceforge.net/docs/user/rst/quickref.html) reference from docutils.
- [ReST cheat sheet](https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html) by Thomas Cokelaer.
- [Sphinx](http://www.sphinx-doc.org/) documentation, including reference on Sphinx-specific ReST syntax.

As the scope of the repository states - please do not store your data in the repository itself. Good places to upload files such as videos or presentation slides might be http://pure.iiasa.ac.at/id/eprint/17286/ or https://data.ene.iiasa.ac.at/. Then simply link to the folder within your ReST file. 

E.g. linking a video:

```
.. raw:: html

	<video width="640" height="360" controls preload="none" controlsList="nodownload">
		<source src="Your file path" type="video/mp4">
 ```
