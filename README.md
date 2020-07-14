# UCD Thesis/Dissertation Template

## About
The following set of files are the components needed to write your thesis or dissertation using Latex for the University of California, Davis.  

Originally based on the File for a general UC Dissertation / Thesis  
Modfied specifically to the UCD thesis class by Shwaine <shwaine@shwaine.com>  

* 2006 - More recent changes by Dylan Beaudette  
* 2010 Clarification and posting to github by Alex Mandel <tech@wildintellect.com>  
* 2011 E-filing tweak by Jason Moore  
* 2014 Style updates to fit recent requirements (See the Changelog for more details)  
* 2019 - some changes by Stephen Maples  
* 2020 - additional changes by Rich Pauloo

## Quickstart

```
git clone https://github.com/richpauloo/thesis.git
cd Github/thesis

pdflatex -synctex=1 -interaction=nonstopmode thesis.tex
biber thesis.tex
pdflatex -synctex=1 -interaction=nonstopmode thesis.tex
```

Note that `thesis.tex` lines 14 and 15 are used to compile the draft (much faster) and final (much slower) versions.  

```
\documentclass[11pt,oneside,draft]{ucdthesis} 
%\documentclass[11pt,oneside,final]{ucdthesis}
```

## How to write your thesis
 * Download Source (button above)
 * Using your favorite Latex Editor
	* Edit the Chapter files, add more if you need (also add reference in the thesis.tex)
	* Edit the Abstract and Title matter documents
 * Build your latex document using pdflatex
	* Run `pdflatex thesis.tex` (rerun if the table of contents isn't updating)
	* Run `bibtex thesis.tex` (important that the engine is `biber`, and rerun when you change refs)
	* Run `pdflatex thesis.tex`
 * To get a bibliography you need to run bibtex on your main document.
 	* If you have bibliographies per chapter you also need to run bibtex per chapter
	* After running bibtex on everything rerun pdflatex 
 * There are many optional sections: use the % character to toggle commenting out parts you don't need.
	* Dedication
	* Acknowledgments
	* Preface
