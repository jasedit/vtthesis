# Overview

This repository contains a LaTeX template that matches the requirements of Virginia Tech's Electronic Thesis and Dissertation (ETD) repository. This template has been refactored to integrate with the MultiMarkdown LaTeX conversion system, for easier writing.

# Instructions

This template integrates with the paper system available [here](https://github.com/jasedit/papers_base). This template can be cloned into a directory under the templates directory, and then used by having the following lines in the MMD metadata:

```
latex input: vtthesis/setup.tex
latex footer: vtthesis/footer.tex
```