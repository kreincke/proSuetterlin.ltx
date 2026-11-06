<!--
% This file is part of proSuetterlin.ltx
% (c) 2022ff Karsten Reincke (https://github.com/kreincke/proSuetterlin.ltx)
% It is distributed under the terms of the Creative Commons license
% CC-BY-4.0 (= https://creativecommons.org/licenses/by/4.0/)
-->

<p align="center">
    <a href="https://github.com/kreincke/proSuetterlin.ltx/commits/" title="Last Commit"><img src="https://img.shields.io/github/last-commit/kreincke/proSuetterlin.ltx?style=flat"></a>
    <a href="https://github.com/kreincke/proSuetterlin.ltx/issues" title="Open Issues"><img src="https://img.shields.io/github/issues/kreincke/proSuetterlin.ltx?style=flat"></a>
    <a href="https://github.com/kreincke/proSuetterlin.ltx/blob/master/LICENSE" title="License"><img src="https://img.shields.io/badge/License-CC_BY_4.0-blue.svg?style=flat"></a>
</p>

<p align="center">
  <a href="#use">Use</a>  
  <a href="#structure">Structure</a>  
  <a href="#prerequisites">Prerequisites</a>  
  <a href="#background">Background</a>  
  <a href="#contributions">Contributors</a>  
  <a href="#licensing">Licensing</a>
</p>

![the proSuetterlinLogo](img/logo.png)

***proSuetterlin.ltx*** offers a set of configuration- and template-files to use the old German handwriting in *LaTeX*-Files, particularly in texts of the relevant humanities disciplines. It is primarily aimed at German speaking and writing people/scientists. 

## Use

For setting up ***proSuetterlin.ltx*** successfully:

0. Install a complete TexLive-Distro including pdflatex and xelatex as LaTeX-Engines.
1. Clone the ***proSuetterlin.ltx*** repository `git clone https://github.com/kreincke/proSuetterlin.ltx` (or download and extract the respective tarball)
2. Open a shell, change into the ***proSuetterlin.ltx*** directory and erase the directory `.git`
3. Call `make` to verify that the system is running
4. Open and close your *JabRef* version once.
5. Call `find $HOME -type f | grep jabref | grep customizedBiblatexTypes` to determine, where your *JabRef* configuration files are stored
6. Copy `cfg/jabref-prefs.xml` to `$HOME/.java/.userPrefs/org/jabref/prefs.xml` (or wherever your systems stores the general JabRef configurations)
7. Copy `cfg/jabref-customizedBibLatexTypes-prefs.xml` to `$HOME/.java/.userPrefs/org/jabref/customizedBiblatexTypes/prefs.xml` (or wherever your systems stores the BibLatex / Bibtex literature specifications)
8. Edit `suetterlin.tex` and throw away what you do not need.


## Structure

Particularly, ***proSuetterlin.ltx*** contains files
* to configure LaTeX and Biber in accordance with the rules of the classical philology
  - `cfg/inc.cfg-biber-de.tex`
* to configure jabref (5.x) in accordance with the classical philology
  - `jabref-prefs.xml`
  - `jabref-customizedBibLatexTypes-prefs.xml`
  - `biber-jabref-types.md`
* to integrate an index of abbreviations
  - `cfg/inc.cfg-ncl-de.tex`ls
  - `cfg/nomencl.ist`
* to overwrite automatically applied hyphenations
  - `cfg/inc.babelhyphenations.tex`


Finally, ***proSuetterlin.ltx*** contains
* `bib/lit.main.bib` (= stores the bibliographic data of the secondary literature, can be edited by a respectively configured *jabref* or a plain text editor, is integrated into the final text by the command LaTeX-command `\addbibresource`)
* `bib/lit.verify.bib` (= contains two entries to verify the citation style of German humanities)
* `bib/ncl.abbreviations-de.tex` respectively `bib/ncl.abbreviations-en.tex` (= stores general abbreviations, can be edited by any text editor, is added by the LaTeX command `\input{bib/ncl.abbreviations-[de|en].tex}`
)
* `bib/ncl.journals.tex`(= stores journal specific abbreviations, can be edited by any text editor, is added by the LaTeX command `\input{bib/ncl.journals.tex}`


## Prerequisites

*proSuetterlin.ltx* requires the installation of

* a LaTeX distribution with different packages/programs which should be part of your TeX-Distribution:
  * BibLatex : [https://ctan.org/pkg/biblatex](https://ctan.org/pkg/biblatex)
  * Biber : [https://github.com/plk/biber](https://github.com/plk/biber)
  * biblatex-dw [https://ctan.org/pkg/biblatex-dw](https://ctan.org/pkg/biblatex-dw)
  * Koma-Script : [https://www.ctan.org/pkg/koma-script](https://www.ctan.org/pkg/koma-script)
* bash
* make

## Background

*proSuetterlin.ltx* is a derivation work of *proScientia.ltx*. For adopting the working and writing style of German Scholars sucessfully, have a loog at [https://github.com/kreincke/proScientia.ltx](https://github.com/kreincke/proScientia.ltx)

## Contributions

Contributions to *proSuetterlin.ltx* are welcome. Please use the methods of GitHub to do so. But your contributions also have to be licensed under the *CC BY 4.0*.

## Licensing

Copyright (C) 2026 Karsten Reincke

*proSuetterlin.ltx* is distributed under the terms of the [**CC BY 4.0**](https://creativecommons.org/licenses/by/4.0/) license; you may not use this project except in compliance with that license. You are free to ...

* share (= copy and redistribute the material in any medium or format)
* adapt (= remix, transform, and build upon the material for any purpose, even commercially).

*proSuetterlin.ltx* under the following terms:

* You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

* You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits (= *No additional restrictions*)

### Clarifications

*proSuetterlin.ltx* is a set of template files and is intended to be instantiated and reused in the user's scientific work. Therefore, we decide:

1. Instantiating *proSuetterlin.ltx* files and reusing them in one's own (scientific) writing project does not make this writing project a derivative work of *proScientia.ltx* (hence: you do not have to mark your modifications in your project directory)  
2. But if you distribute a modified version of *proSuetterlin.ltx* as a non-instantiated set of templates (as you've got it), you must mark your modifications  
3. The requirement *to give appropriate credit and provide a link to the license* can be fulfilled by adding a note to your work like this:
  * Erstellt  auf der Basis des CC-BY-4.0 lizenzierten Tools **proScientia** von K. Reincke © 2026 Repository: [https://github.com/kreincke/proSuetterlin.ltx](https://github.com/kreincke/proScientia.ltx),
Lizenztext [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * Developed on the base of the CC-BY-4.0 licensed tool **proSuetterlin.ltx** by K. Reincke  © 2026 [
repository = [https://github.com/kreincke/proSuetterlin.ltx](https://github.com/kreincke/proScientia.ltx),
license text = [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/) ]
