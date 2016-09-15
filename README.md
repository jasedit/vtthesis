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
3. `bibtex`, `$BIBTEX` - defines the Bibtex file to process for this document. Delete this line to eliminate bibliography support
4. `myreporttype`, `$REPORTTYPE` - The document type displayed on the cover page, should be either `Thesis` for Masters students or `Dissertation` for PhD students
5. `mydegree`, `$DEGREE` - The degree that is being awarded with this document. This should be the full degree, so `Masters of Science`, not simply `Masters`.
6. `mydepartment`, `$DEPARTMENT` - The Department which is awarding this degree

## LaTeX/Metadata Variables

1. `myabstract` - if this LaTeX variable is defined, the variable will be inserted as the abstract for the paper. This overrides the `abstract` variable
2. `abstract` - if this LaTeX variable is defined, include the contents of the file named as the abstract.
3. `myacknowledgements`, `$ACKNOWLEDGEMENTS` - If defined, the value of this variable will be inserted as acknowledgements
4. `mykeywords`, `$KEYWORDS` - Keywords which are inserted into the document for metadata purposes
5. `mycommittee`, `$COMMITTEE` - List of committee members to place on cover page. This is unfiltered, so raw LaTeX is fully supported for multi-line and odd names
