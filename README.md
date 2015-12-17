# Ten Simple Rules for taking advantage of GitHub in bioinformatics

## Description 

This repository contains the manuscript entitle: **Ten Simple Rules
for taking advantage of GitHub in bioinformatics**. Our main aim here
is to highlight specific GitHub features that enable the
bioinformatics community to use GitHub features and tools on a daily
basics. We will then provide a set of recommendations for taking full
advantage of its core features to facilitate and manage the work on a
given bioinformatics project and increase its profile to the
scientific community. We think the manuscript is timely due to the
announcement of the closure of another widely used service, Google
Code. Therefore, many of the users of Google Code will therefore have
to migrate to GitHub.

# How to contribute 

**We currently do not accept additional contributions as the
  manuscript is submitted. If you have any comments or suggestions,
  please open an issue to discuss them.**

If you have an idea for a new Rule to add or change to the main
manuscript or Figure, etc, it is best to communicate with the authors
of the paper. The most common venues for this are GitHub issues for
common specification
[issues](https://github.com/ypriverol/github-paper/issues). Browse
through existing GitHub issues and if one seems related, comment on
it. If no existing issue seems appropriate, a new issue can be opened
to discuss the suggestion.

## Changes and Ideas

All changes to the manuscript should be made through pull requests to this repository. 

If you are new to Git, the
[Try Git](https://www.codeschool.com/courses/try-git) tutorial is a
good places to start. More learning resources are available
[here](https://help.github.com/articles/good-resources-for-learning-git-and-github/).

1. Create a GitHub account and log in.

2. Fork the paper repository on GitHub to make your changes. 

3. Choose the correct branch to develop your changes against or create
   a new one (this is typically `master`).

4. Serious problems or major changes should not be fixed via pull
   request - please open an issue an specifically tag `@ypriverol` to
   discuss such changes beforehand.

5. Commit and push your changes to your fork.

6. Open a pull request with these changes. You pull request message
   ideally should include:
   - A motivation of why the changes should be made.
   - A brief description of the changes.

7. The pull request should be reviewed and merge by another member of
   the paper.

## Conversion to PLoS LaTeX

- **Any modifications should be made to the `manuscript.md` file.**
  This file is then converted to LaTeX using `pandoc`:

```
make manuscript.tex
```

- Then include the text from `manuscritp.tex` (ignore title, authors
  and references) into `manuscript-plos.tex`.

- Comment the figure inclusion line.

```
% \includegraphics[width=\linewidth]{../figures/figure01_overview.pdf}
```

- Compile by running

```
make manuscipt-plos.pdf
```

- Only commit `manuscript-plot.tex` and `manuscript-plos.pdf` to the
  repo. To clean up unwanted files:

```
make clean
```

## Disclaimer

The authors have no affiliation with [GitHub](https://github.com/),
nor any commercial entity mentioned in this articel. The views
described here reflect our owns without any input from any third party
organisation.
