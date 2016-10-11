# Overview

This repository contains a LaTeX template that matches the requirements of Virginia Tech's Electronic Thesis and Dissertation (ETD) repository. This template has been refactored to integrate with the MultiMarkdown LaTeX conversion system, for easier writing.

# Instructions

This template integrates with the paper system available [here](https://github.com/jasedit/papers_base). This template can be cloned into a directory under the templates directory, and then used by having the following lines in the MMD metadata:

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
4. `bibtex`, `$BIBTEX` - defines the Bibtex file to process for this document. Delete this line to eliminate bibliography support
5. `myreporttype`, `$REPORTTYPE` - The document type displayed on the cover page, should be either `Thesis` for Masters students or `Dissertation` for PhD students
6. `mydegree`, `$DEGREE` - The degree that is being awarded with this document. This should be the full degree, so `Masters of Science`, not simply `Masters`.
7. `mydepartment`, `$DEPARTMENT` - The Department which is awarding this degree

## LaTeX/Metadata Variables

1. `myacknowledgements`, `$ACKNOWLEDGEMENTS` - If defined, the value of this variable will be inserted as acknowledgements
2. `mykeywords`, `$KEYWORDS` - Keywords which are inserted into the document for metadata purposes
3. `mycommittee`, `$COMMITTEE` - List of committee members to place on cover page. This is unfiltered, so raw LaTeX is fully supported for multi-line and odd names
4. `mylinespace` - If defined, sets the line spacing of the document using the [setspace](http://www.ctan.org/tex-archive/macros/latex/contrib/setspace/) package.
