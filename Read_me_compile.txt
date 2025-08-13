Important:
To avoid errors and problems when compiling, please always use the current version of your operating system (Windows / Mac / Linux), the current version of your LaTeX distribution (MiKTeX / MacTeX / Tex Live) and the current version of your typesetting program or LaTeX editor (TeXstudio / Texmaker / TeXworks / TeXnicCenter). Update your operating system, your LaTeX distribution and your LaTeX editor before compiling this template or have them updated by your department IT representative.




Notes on compile / setting order:
For the correct display of the layout and the bibliographies (multibib) please compile as follows (see "Order of compilation operations"):

- Windows 10: via the PowerShell or command prompt (cmd).
To do this, go to the folder of this project, do not select any file, click on an empty space with the left mouse button and open the context menu while holding down the Shift key (Shift key + right mouse click) and select "Open PowerShell window here". Then enter "cmd" and call the compile processes individually as follows (see "Order of compilation operations"):

- macOS Big Sur: via the terminal.
To do this, go to the parent folder of this project and select the folder in which the project is located. Now open the context menu (secondary click) by pressing Control + mouse button or tapping with two fingers on the trackpad. Now select "New Terminal at Folder" and call up the compile processes individually as follows:




Order of compilation operations:
 pdflatex KSP_Diss_17x24
 bibtex KSP_Diss_17x24
 bibtex journal					% The file name of the file to be executed with Bibtex is specified in the command "\ newcites {}" in this TeX file
 bibtex conference				% The file name of the file to be executed with Bibtex is specified in the command "\ newcites {}" in this TeX file
 pdflatex KSP_Diss_17x24
 pdflatex KSP_Diss_17x24




Notes on TeXstudio:
Permanently change the compilation calls in TeXstudio (Windows 10, TeXstudio 3.0.1):
Options / Configure TeXstudio ... / Build / -> And here adjust the entries "Default Compiler" and "Default Bibliography Tool".

Execute the compilation calls manually in TeXstudio (Windows 10, TeXstudio 3.0.1):
Tools / Commands / -> And here the entries "PDFLaTeX" and "Bibtex" (Bibtex, however, cannot be executed for certain files in TeXstudio; the input prompt must be used for this (see above).




Bibliography, bibliography and citation style:
Please note that the bibliography and citation style in this template are unlikely to meet the requirements of your institute. Due to the variety of different styles, this LaTeX template cannot provide a precisely defined bibliography and citation style for individual inquiries. Please use the LaTeX packages provided by your institute for the styles you are using and adapt the bibliography style "\bibliographystyle{plainnat}" in the file "Contents/Bibliography.tex" as well as the citation style "\usepackage{natbib}" in the file "KSP_Diss_17x24_EN.tex" according to your needs.

If you do not want to automatically output all titles from your file with the bibliographic information (e.g. "Bibliography/Literature.bib") in the bibliography, please remove the commands "\nocite{*}" or "\nocitejournal{*}" and "\nociteconference{*}" from the file "Contents/Bibliography.tex".

The counter for the titles in the bibliography (e.g. "Journal articles" or "Conference contributions") is reset to "[1]" by default by the optional parameter "resetlabels" for the command "\usepackage[resetlabels]{multibib}" in the file "KSP_Diss_17x24_EN.tex". If you want the titles for the bibliography to be numbered consecutively, please remove the optional parameter "resetlabels" in the above command.
