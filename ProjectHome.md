This program converts HTML documentation trees into Texinfo format.

Given the name of a main (or contents) HTML file, it processes that file,
and other files (transitively) referenced by it, into a Texinfo file (whose
name is chosen from the file or directory name of the argument).  For
instance:
```
  html2texi.pl api/index.html
```
produces file "api.texi".
After producing the `.texi` file, before processing it with makeinfo or TeX
you should update the menus and nodes; in Emacs, do `C-u C-c C-u C-a`.

Texinfo format can be easily converted to Info format (for browsing in
Emacs or the standalone Info browser), to a printed manual, or to HTML.
Thus, `html2texi.pl` permits conversion of HTML files to Info format, and
secondarily enables producing printed versions of Web page hierarchies.

Unlike HTML, Info format is searchable.  Since Info is integrated into
Emacs, one can read documentation without starting a separate Web
browser.  Additionally, Info browsers (including Emacs) contain
convenient features missing from Web browsers, such as easy index lookup
and mouse-free browsing.