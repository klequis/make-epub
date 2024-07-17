
```
pandoc test1.md -f markdown -t html -s -o test1.html
```

-s | standalone file with header and footer
-o | output file
-f | from format
-t | to format


Install *texlive*:

```
sudo apt install texlive-latex-extra
```

If multiple input files are given, pandoc will concatenate them all (with blank lines between them) before parsing. (Use `--file-scope` to parse files individually.)


## ePub

epub or epub3 (EPUB v3 book)
epub2 (EPUB v2)

- If I use `epub` do I get `epub3`?

## Create PDF

This creates the PDF with formatting

```
pandoc -c theme.css test1.md -o test.epub
```

But:
By default, pandoc will use LaTeX to create the PDF, which requires that a LaTeX engine be installed (see --pdf-engine below). Alternatively, pandoc can use ConTeXt, roff ms, or HTML as an intermediate format. To do this, specify an output file with a .pdf extension, as before, but add the --pdf-engine option or -t context, -t html, or -t ms to the command line. The tool used to generate the PDF from the intermediate format may be specified using --pdf-engine.

You can control the PDF style using variables, depending on the intermediate format used: see variables for LaTeX, variables for ConTeXt, variables for wkhtmltopdf, variables for ms. When HTML is used as an intermediate format, the output can be styled using --css.

## Chunked HTML
pandoc `-t chunkedhtml` will produce a zip archive of linked HTML files, one for each section of the original document. Internal links will automatically be adjusted to point to the right place, images linked to under the working directory will be incorporated, and navigation links will be added. In addition, a JSON file sitemap.json will be included describing the hierarchical structure of the files.

## Syntax highlighting

```
--highlight-style=STYLE|FILE
```

Specifies the coloring style to be used in highlighted source code. Options are pygments (the default), 
- kate, 
- monochrome, 
- breezeDark, 
- espresso, 
- zenburn, 
- haddock, 
- tango

```
--syntax-definition=FILE
--syntax-definition=javascript-react.xml
```

Instructs pandoc to load a KDE XML syntax definition file, which will be used for syntax highlighting of appropriately marked code blocks. This can be used to add support for new languages or to use altered syntax definitions for existing languages. This option may be repeated to add multiple syntax definitions.


## Example header

---
title: Title
author: Carl
rights: Copyright Carl
lang: en-US
---



## From video

Create slides
```
pandoc -t beamer -V theme=Verlin -V colortheme=seahorse document.md document.pdf
```