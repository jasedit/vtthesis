# Overview

This repository contains a LaTeX template that matches the requirements of Virginia Tech's [Electronic Thesis and Dissertation](http://etd.vt.edu/) (ETD) repository. This template has been refactored to integrate with [scriptorium](https://github.com/jasedit/scriptorium), for easier writing.

# Instructions

After installing scriptorium, this template can be installed with the command:

```
scriptorium template -i https://github.com/jasedit/vtthesis.git
```
And a new paper created in the directory `$paper` using this template by executing:

```
scriptorium paper new -t vtthesis $paper
```

Or, to shift an existing paper to this template, ensure the two lines in the document frontmatter including the LaTeX files read:

```
latex input: vtthesis/setup.tex
latex footer: vtthesis/footer.tex
```

# Template Variables

Variables have two potential configuration points, which will be described here. The first point is the frontmatter variable name, which is used by the underlying system to identify the value at build time. The second point is the placeholder value, which can be replaced during the new command, or manually edited later. For the following description, variables will be named in the format `Variable Name, Placeholder Name - Description`

## MultiMarkdown Frontmatter
1. `latex author`,`$AUTHOR` - name of the paper author
2. `latex title`, `$TITLE` - title of the document
3. `my abstract`, `$ABSTRACT` - defines the name of the file to include directly into the LaTeX output as the abstract
4. `my public abstract`, `$PUBLIC_ABSTRACT` - define the name of the file to include directly into the LaTeX output as the abstract
5. `bibtex`, `$BIBTEX` - defines the Bibtex file to process for this document. Delete this line to eliminate bibliography support
6. `myappendices`, `$APPENDICES` - defines the name of the file to include directly into the LaTeX output as the appendices. Not required.
6. `myreporttype`, `$REPORTTYPE` - The document type displayed on the cover page, should be either `Thesis` for Masters students or `Dissertation` for PhD students
7. `mydegree`, `$DEGREE` - The degree that is being awarded with this document. This should be the full degree, so `Masters of Science`, not simply `Masters`.
8. `my department`, `$DEPARTMENT` - The Department which is awarding this degree
9. `my packages` - If defined, includes the value of this key as a filename in the document preamble, allowing for custom packages and commands to be included
10. `my glossary` - If defined, includes the named file and enables glossary support using the [glossaries](https://www.ctan.org/pkg/glossaries) package.
11. `my date` - If defined, is the string which is used to represent the date on the title page.

## LaTeX/Metadata Variables

1. `myacknowledgements`, `$ACKNOWLEDGEMENTS` - If defined, the value of this variable will be inserted as acknowledgements
2. `mykeywords`, `$KEYWORDS` - Keywords which are inserted into the document for metadata purposes
3. `mycommittee`, `$COMMITTEE` - List of committee members to place on cover page. This is unfiltered, so raw LaTeX is fully supported for multi-line and odd names
4. `mylinespace` - If defined, sets the line spacing of the document using the [setspace](http://www.ctan.org/tex-archive/macros/latex/contrib/setspace/) package.
