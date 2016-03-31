# Ten Simple Rules for taking advantage of GitHub [![Build Status](https://travis-ci.org/tompollard/github-paper.svg?branch=master)](https://travis-ci.org/tompollard/github-paper)

## Description 

This repository contains the manuscript entitled:
[**Ten Simple Rules for taking advantage of GitHub (in bioinformatics)**](https://github.com/ypriverol/github-paper/blob/master/document/manuscript.md). Our
aim here is to describe how the bioinformatics community can use
GitHub features and tools on a daily basis.

## Commenting and contributing 

We are about to re-submit the manuscript after addressing the
reviewers' comments, but would appreciate input from the community by
discussing any points through GitHub
[issues](https://github.com/ypriverol/github-paper/issues) and/or pull
requests.

Feel free to browse through existing/past issues and if one seems
related, comment on it. If no existing issue seems appropriate, a new
issue can be opened to discuss the suggestion. In particular, we would
appreciate discussing more substantial changes (for example suggestion
of new rules) in a dedicated issue before sending a pull request.

If you are new to Git, read the
[manuscript](https://github.com/ypriverol/github-paper/blob/master/document/manuscript.md)
and
[*A Quick Introduction to Version Control with Git and GitHub*](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004668) -
your input would be most valuable.

If, based on your contribution, you would like to be added as a
co-author, please open an issue and provide your name and affiliation
and a short description of your contribution or a link to the relevant
issue and pull request.

## Conversion to PLoS LaTeX

- **Any modifications should be made to the `manuscript.md` file.**
  This file is then converted to LaTeX using `pandoc`:

```
make manuscript.tex
```

- Then include the text from `manuscript.tex` (ignore title, authors
  and references) into `manuscript-plos.tex`.

- Comment the figure inclusion line.

```
% \includegraphics[width=\linewidth]{../figures/figure01_overview.pdf}
```

- Compile by running

```
make manuscript-plos.pdf
```

- Only commit `manuscript-plos.tex` and `manuscript-plos.pdf` to the
  repo. To clean up unwanted files:

```
make clean
```

## Disclaimer

The authors have no affiliation with [GitHub](https://github.com/),
nor any commercial entity mentioned in this article. The views
described here reflect our own views without input from any third party
organisation.
