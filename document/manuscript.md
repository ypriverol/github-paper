# Ten Simple Rules for taking advantage of git and GitHub

Yasset Perez-Riverol (1)[^1], Rui Wang (1), Timo Sachsenberg (2), Julian Uszkoreit (3), Laurent Gatto (4), Felipe da Veiga Leprevost (5), Christian Fufezan (6), Tobias Ternent (1), Juan Antonio Vizcaíno (1)[^2]

(1) European Molecular Biology Laboratory, European Bioinformatics Institute (EMBL-EBI), Wellcome Trust Genome Campus, Hinxton, Cambridge, CB10 1SD, UK.

(2) Applied Bioinformatics and Department of Computer Science, University of Tübingen, D-72074 Tübingen, Germany.

(3) Medizinisches Proteom-Center, Ruhr-Universität Bochum, Universitätsstr. 150, D-44801 Bochum, Germany.

(4) Computational Proteomics Unit, Cambridge Systems Biology Centre, University of Cambridge Tennis Court Road Cambridge, CB2 1GA, UK.

(5) Department of Pathology, University of Michigan, Ann Arbor, Michigan 48109, USA.

(6) Institute of Plant Biology and Biotechnology, University of Muenster, Schlossplatz 8, 48143 Muenster, Germany.

[^1]: yperez@ebi.ac.uk.
[^2]: juan@ebi.ac.uk.


Short title: Ten Simple Rules for taking advantage of GitHub

## Introduction

Bioinformatics is a broad discipline in which the common denominator
is the need to produce and/or use software that can be applied to
biological data in different contexts. To enable and ensure the
replicability and traceability of scientific claims, it is essential
that the scientific publication, the corresponding datasets and the
data analysis are made publicly available
\cite{Goodman:2014,Perez-Riverol:2015}. All software used for the
analysis should be either carefully documented (e.g. for commercial
software) or, better, openly shared and directly accessible to others
\cite{Osborne:2014,Vihinen:2015}.  The rise of openly available
software and source code, and concomitant collaborative development is
facilitated by the existence of several code repository services such
as SourceForge (http://sourceforge.net/), Bitbucket
(https://bitbucket.org/), GitLab (https://about.gitlab.com/) and
GitHub (https://github.com/), among others. These resources are also
essential for collaborative software projects, since they enable the
organisation and sharing of programming tasks between different remote
contributors. Here, we introduce the main features of GitHub, a
popular web-based platform which offers a free and integrated
environment for hosting the source code, documentation and
project-related web content for open source projects. GitHub also
offers paid plans for private repositories for individuals and
businesses, as well as free plans including private repository for
research and educational use. 

GitHub relies, at its core, on the well-known and open source version
control system git, designed by Linus Torvalds for the development of the Linux kernel. 
Nowadays, git is developed and maintained by the git community (https://github.com/git).
One reason for GitHub's success is that it offers more than a simple source code hosting service
\cite{blischak2016quick, ram2013git}. It provides developers and
researchers with a dynamic and collaborative environment, often referred 
to as a social coding platform, with the ability to review, comment and
discuss code \cite{Dabbish:2012}. Individual bioinformatics projects such as `MSnbase`
(https://github.com/lgatto/MSnbase) \cite{Gatto15012012} and `waverepo`
(https://github.com/sje30/waverepo) \cite{Eglen:2014}), lab
repositories (for example https://github.com/PRIDE-Toolsuite/ 
\cite{Perez-Riverol01012016}), intermediate and large projects such as 
samtools (https://github.com/samtools), OpenMS (https://github.com/OpenMS)
\cite{sturm2008openms} and the Galaxy project (https://github.com/galaxyproject/galaxy/) 
\cite{Goecks:2010}, or global collaborations such as rOpenSci
(https://github.com/ropensci) and The Global Alliance For Genomics and
Health (https://github.com/ga4gh) have found the perfect place in
GitHub to share code, ideas and collaborate (see Table 1).

Some of our recommendations outlined below are applicable to other
hosting services. However our main aim here is to highlight specific
GitHub features. We provide a set of recommendations to take full
advantage of GitHub's features to manage small and large
bioinformatics projects and increase their profile and
visibility. These rules have been ordered to reflect a typical
development process: learning git and GitHub basics, collaboration,
use of branches and pull requests, labelling and tagging of code
snapshots, tracking project bugs and enhancements using issues, and
dissemination of the final results.

## Rule 1. Use GitHub to track your projects

The cornerstone of GitHub is the distributed version control system
git. Every change, from fixing a typo to a complete redesign of the
software, is tracked and controlled by individual and unique
identifier. While git has a complex set of commands and can be used
for rather complex operations, learning and apply the basics only
requires a handful of new concepts and commands, and will provide a
solid ground to efficiently track your coding and research
projects. Many introductory and detailed tutorials are available (see
Table 1 below for a few examples). In particular, we recommend *A
Quick Introduction to Version Control with Git and GitHub* by Blischak
*et al.* \cite{blischak2016quick}.

In a nutshell, initialising a (local) repository (often abbreviated
_repo_) marks a directory as one to be tracked (Fig. 1). All or parts
of its content can be added explicitly to the list of files to track.

```
cd project ## move into directory to be tracked
git init   ## initialise local repository
## add individual files such as project description, reports, source code
git add README project.md code.R 
git commit -m "initial commit" ## saves the current local snapshot 
```

From now on, every change to these tracked files, once committed, will
be recorded as a new revision, or _snapshot_, uniquely identifying the
changes in all the modified files. Git is remarkably effective in
archiving the complete history of a project (all revisions) by,
amongst other things, storing only the differences among them.

In addition to local copies of the repository, it is easy to create
remote repositories on GitHub (called `origin`, with default branch
`master` - see below) using the web interface, and then synchronise
local and remote repositories.

```
git push origin master ## push local changes to the remote repo
git pull origin master ## pull remote changes into the local repo
```

Following Tony Rossini's advice in 2005 to "commit early, commit often, and commit in 
a repository from which we can easily roll-back your mistakes", one can keep track of the development in small incremental
changes. At any time it is possible to go back to a previous
version. In larger projects, multiple users contribute to the same
remote repository and all their contributions are recorded, attributed
and can be restores.

Users usually track source code, text files, images and small data
files inside their repos. And while the majority of GitHub
repositories are used for software development, there is nothing
preventing users from keeping text documents such as analysis reports
and manuscripts (see for example the repository for this manuscript at
https://github.com/ypriverol/github-paper), or other file types in
your projects. 

The web interface offered by GitHub provides a friendly interface to
many basic operations and a gentle introduction to a more rich albeit
complex set of functionalities. There exists also various graphical
user-interface driven clients to manage git and GitHub repositories
(https://www.git-scm.com/downloads/guis). Many editors and
development environments such as, for example, the popular Rstudio editor
(https://www.rstudio.com/) for the R programming language \cite{R},
directly integrate with code versioning using git and GitHub. In
addition for remote git repositories, GitHub provides its own features
that will be described in subsequent rules (Fig. 1).

![The structure of a GitHub-based project illustrating project structure and interactions with the community.](./figure01_overview.pdf)

> **Box 1** Using GitHub, or any similar versioning/tracking system is
> not a replacement for good projects management; it is an extension,
> an improvement for good project and file managing (see for example
> \cite{Noble:2009}). One practical consideration, when using GitHub,
> for example, is dealing with large binary files.  Binary files such
> as images, videos, executable files or many raw data used in
> bioinformatics, are stored as a single large entity in git.  As a
> result, every change, even if minimal, leads to a complete new copy
> of the file in the repository, producing large size increments and
> the inability to search (see
> https://help.github.com/articles/searching-code/) and compare file
> content across revisions. Git offers a Large File Storage (LFS)
> module (https://git-lfs.github.com/) that replaces such large files
> with pointers, while the large binary file can be stored remotely,
> which results in small and faster repositories. Git LFS is also
> supported by GitHub, albeit with a space quota or for a fee, to
> retain your usual GitHub workflow
> (https://help.github.com/categories/managing-large-files/)
> (Supplementary Note, Section 1).

> **Box 2** TODO Public of private repositories -
> see [issue 111](https://github.com/ypriverol/github-paper/issues/111).

## Rule 2. GitHub for single users, teams and organisations

Open source projects on GitHub are visible to everyone, but write
permissions, i.e. the possibility to directly modify the content of a
repo, need to explicitly be granted. As a repository owner, you can
grant these rights to other GitHub users. In addition to being owned
by users, repositories can also be created and managed as part of
teams and organisation.

Project managers can structure projects to manage permissions at
different levels: users, teams and organisations.  Users are the
keystone of GitHub, as in any other social network. Every user has a
profile listing their GitHub projects and activities, which can be
populated optionally with personal information including name, e-mail
address, image and webpage. To stay up to date with the activity of
other users one can _follow_ their accounts (see also Rule
10). Collaboration can be achieved by simply adding a trusted
_Collaborator_ and thereby granting write access.

However, development in large projects is usually done by teams of
people, within a larger organisation. GitHub organisations are a great
way to manage team-based access permissions for the individual
projects of institutes, research labs, and large open source projects
that need multiple owners and administrators (Fig.  1). We recommend
that you (as an individual researcher) make your profile visible to
other users and display all the projects and organisations you are
working in, including a list of the latest activities on the site
(Fig. 1).

## Rule 3. Developing and collaborating on new features: branching and forking

Everyone with a GitHub account can _fork_ any public repository and
start developing the same code base in one's own fork
(https://help.github.com/articles/fork-a-repo/) under their username
(see for example
https://github.com/ypriverol/github-paper/network/members for this
work) or organisation (see Rule 2). A fork is a complete copy of a
repository content that retains a link to the original
repository. Forking a repository allows you to freely experiment with
changes without affecting the original project. This forking is the
basis of social coding. It allows anyone to develop and test novel
features into existing code and offers the possibility to contribute
(by opening _pull requests_) novel features, improvement to
documentation or simple typo corrections
(https://twitter.com/rgfitzjohn/status/708309767240982528) back the
into the original (upstream) project, thereby improving the original
repository and becoming a contributor. Forking a repository and
providing pull requests constitute an easy way for collaboration
inside loosely defined teams and over more formal organisation
boundaries, while the original repository owner(s) retain control over
which external contributions to include. Once a pull request is opened
for review and discussion, it usually results in additional insights
and increased code quality.

Concurrent development including commits to the same
repository can be organised using different approaches. The most
common way is to use git _branches_ to separate different lines of
development. Active development is often performed on a development
branch and stable versions e.g. those used for a software release,
are kept in a master or release branch (see for example https://github.com/OpenMS/OpenMS/branches). 
In practice, developers work on one or several features or improvements. To keep commits of the different
features logically separated, distinct branches are typically
used. Later, when development is complete and none of the tests fail
(see Rule 5) new features can be merged back into the development line
or master branch. In addition, one can always pull the currently up-to-date 
master branch into a feature branch, to adapt the feature to the changes 
in the master branch.

When developing different features in parallel, there is a risk to
apply incompatible changes in different branches/forks; these are said
to become out of sync. Branches are just short-term departures from
master. If you pull frequently, you will keep your copy of the repo up
to date, and you will have the opportunity to merge your changed code
with others' contributors without requiring to manually address
conflicts to bring the branches in sync again.

## Rule 4. Naming branches and commits: tags and semantic versions

Tags offer the possibility to label versions during the development
process. Version numbering should follow
semantic versioning in the form X.Y.Z, with X being the major, Y the
minor and Z the patch version of the release, including possible meta
information, as described in http://semver.org/. This semantic
versioning scheme provides users with coherent version numbers that
document the extent (bug fixes or new functionality) and backwards
compatibility of new releases. Correct labelling allows developers and
users to easily recover older versions, compare them, or simply use
them to reproduce results described in publications (see Rule 8). This
approach will also help defining a coherent software publication
strategy.

## Rule 5: Let GitHub do some tasks for you: integrate

The first rule of software development is that the code needs to be
ready to use as soon as possible \cite{Leprevost:2014}, remain so
during development, and that it should be well-documented and
tested. In 2005, Martin Fowler defined the basic principles for
continuous integration in software development \cite{FowlerCI}. These
principles have become the main reference for best practices in
continuous integration, providing the framework needed to deploy
software, and in some way, also data. In addition to mere error-free
execution, dedicated code testing is aimed at detecting possible bugs
introduced by new features, or changes in the code or dependencies, as
well as detecting wrong results, the so called _logic errors_, where
the source code produces a different result compared to what one
intended it to do. Continuous integration provides the way of
automatically and systematically run all of tests in the repository by
checking data and software dependencies and can be automated through
GitHub.

GitHub offers a set of hooks (automatically executed scripts) that are
run after each push to a repository, making it easier to follow the
basic principles of continuous integration. The GitHub web hooks
allows third-party platforms to access and interact with a GitHub
repository and thus to automate post-processing tasks. Continuous
integration can be achieved by _Travis CI_ (https://travis-ci.org), a
hosted continued integration platform that is free for all open source
projects. Travis CI builds and tests the source code using a plethora of
options such as different platforms and interpreter versions
(Supplementary Note, Section 2). Furthermore it offers notifications
which allow your team and contributors to know if the new changes
work, and prevent the introduction of errors in the code (for instance
when merging pull requests), making the repo always ready to
use. 

## Rule 6: Let GitHub do more tasks for you: automate 

There is more than code compilation and testing that can be integrated
into your software project. GitHub hooks can be used to automate
numerous tasks to help improve the overall quality of your project. A
important complement to successful test completion, is to demonstrate
that they cover the existing code base sufficiently. For this task,
the integration of _Codecov_ is recommended (https://codecov.io).
This service will report how much of the code base and which lines of
code are being executed as part of your code tests. The Bioconductor project,
for example, highly recommends packages to implement unit testing to
support developers in their package development and maintenance
(http://bioconductor.org/developers/unitTesting-guidelines/), and
systematically tests the coverage of all its packages
(https://codecov.io/github/Bioconductor-mirror/). One might also
consider to generate the documentation upon code/documentation
modification (Supplementary Note, Section 3). This implies that your
projects provide comprehensive documentation so others can understand,
and contribute back to them. For Python or C/C++ code, automatic
documentation generation can be done using sphinx
(http://sphinx-doc.org/) and subsequently integrated into GitHub using
"Read the Docs" (https://readthedocs.org/). All of these platforms
will create reports and badges (also called shields) for the projects
that can be included on your GitHub page, thereby making your projects
easily identifiable as high quality and well-maintained.

## Rule 7. Use GitHub to openly and collaboratively discuss, address and close issues

GitHub _issues_ are a great way to keep track of bugs, tasks, feature
requests and enhancements. Classical issue trackers are primarily
intended to be used as bug trackers. In contrast, GitHub issue
trackers (_issues_) follow a different philosophy: each tracker has
its own section in every repository, and can be used to trace bugs,
new ideas, and enhancements, by using a powerful but optional tagging
system for each issue. _Issues_ main focus is on promoting
collaboration, providing context by using cross-references, and
excellent text formatting for each issue: (i) a title and description,
(ii) colour-coded labels help to categorise and filter issues, (iii)
milestones, (iv) one assignee responsible for working on the issue,
and (v) comments that allow anyone with a github account to provide
feedback. Another aspect is its simplicity. For instance, it does not
require one to fill out lengthy forms including every piece of
information that might be valuable to reproduce a bug. It only
requires a title and provides space for optional text (comments). If
the developer needs more information, they can simply request it in a
comment. Alternatively, it is possible for repository administrators
to create issue and pull requests (see Rule 3) templates
(https://help.github.com/articles/helping-people-contribute-to-your-project/)
to customise and standardise the information to be included when
contributors open issues. GitHub issues are dynamic and pose a lower
barrier for users to report bugs and request features. A
well-organised and tagged issue tracker helps upcoming contributors
and users to understand a project more deeply. As an example, the
following issue in OpenMS repository
(https://github.com/OpenMS/OpenMS/issues/1095) allowed the interaction
of eight developers and more than hundred comments. The contributors
can add figures, comments and references to other _issues_ and _pull
requests_ in the repository as well as reference to the code.

As another illustration of _issues_ and their generic and wide
application, we (https://github.com/ypriverol/github-paper/issues) and
others (https://github.com/ropensci/RNeXML/issues/121) used GitHub
issues to discuss and comment changes in manuscripts and address
reviewers' comments.


## Rule 8. Make your code easily citable, and cite source code!

In research, it is good practice to ensure permanent and unambiguous
identifiers for citable items like articles, datasets, or biological
entities such as proteins, genes and metabolites, among
others. Digital Object Identifiers (DOIs) have been used for many
years as unique and unambiguous identifiers for enabling the citation
of scientific publications. More recently, a trend has started to
produce DOIs for other types of scientific outputs such as datasets
\cite{Vizcaino:2014} or training materials (for example
\cite{Ahmadia_2015_27353}). The main motivation behind this is to give
scientists better credit for their work
\cite{NatBiotechEditorial:2009}, enabling at the same time a better
way to cite and track it. In addition, funding agencies such as the
NIH in the USA and Research Councils in the UK, now accept other
research products such as publicly available datasets and software, as
citable research outputs. 

A common issue with software is that it normally evolves at a
different speed than what is published in the scientific
literature. In fact, it is common to find software having novel
features and functionalities that were not described in the original
publication. GitHub now enables the use of DOIs to cite the code
deposited, using the data archiving tool Zenodo
(https://zenodo.org/). The procedure is simple (see
https://guides.github.com/activities/citable-code/) and, by default,
Zenodo takes an archive of a repository each time a new release is
created in GitHub. However, before Zenodo can issue a DOI, metadata
needs to be provided about the archived repository. Once the DOI has
been assigned, you can add it to literature information resources such
as Europe PubMed Central \cite{EuropePMCConsortium:2015}.

As already mentioned in the introduction, reproducibility of
scientific claims should be enabled by providing the software,
the datasets and the process leading to interpretable results that are
used in a particular study. One should always highlight as much as
possible in publications that the code is freely available in,
for example, GitHub, together with any other relevant outputs 
that may have been deposited. In our experience, this
openness substantially increases your chances of getting the paper
accepted for publication. Journal editors and reviewers
have the opportunity to reproduce your findings during the manuscript
review process, increasing the confidence in your results. In addition, once the paper is published, your work can be reproduced
by other members of the scientific community, which can increase
citations and foster opportunities for further discussion and
collaboration. 

Note that the availability of a public repository containing the
source code does not make the software open source _per se_, as it
needs to have an appropriate license (http://opensource.org/licenses/)
that defines how the software can be freely used, modified, and
shared.

## Rule 9. Promote and discuss your projects: web page and more

The traditional way of promoting scientific software is by
publishing them in the peer-reviewed scientific literature. Additional steps can be done to boost the visibility of a
organisation. For example, GitHub _Pages_ are simple landing webpages
that GitHub hosts for free without the need for a server or
database. GitHub users can create and host blog websites, help pages,
manuals, tutorials and websites related to specific projects. _Pages_
comes with a powerful static site generator called Jekyll
(https://jekyllrb.com) that can be integrated with other frameworks 
such as Bootstrap (http://getbootstrap.com/) or platforms such as Disqus
(https://disqus.com/), to support and moderate comments.
In addition, several real-time communication platforms has been integrated with GitHub such as 
Gitter (http://gitter.im) and Slack (https://slack.com/). A real-time communications system allows
the user community, developers and project collaborators to exchange ideas, issues,
report bugs or get support. For example, Gitter is a GitHub-based chat tool which
enables developers and users to share aspects of their work. Gitter
inherits the shape of the social groups operating around GitHub
repositories, organisations, and issues. It relies on the identity
within GitHub, creating IRC (Internet Relay Chat)-like chat rooms for
public and private repositories. From within a Gitter chat, members
can reference issues, comments, or pull-requests. 
GitHub also supports wikis (which are version-controlled repositories
themselves) for each repostitory, where user can create and edit pages
for documentation, examples or general support.


A different service is Gist (https://gist.github.com), which
represents a unique way to share _code snippets_, single files, parts
of files, or full applications. Gist can be generated in two different
ways: public _gists_, that can be browsed and searched, and secret
gists that are not provided through _Discover_
(https://gist.github.com/discover). One of the main features of Gist
is the possibility to embed code snippets in other applications,
enabling users to embed gists in any text field that supports
JavaScript. 

## Rule 10. Use GitHub to be social: follow and watch

One of the main tasks of scientists is to actively follow the developments in
their field. Analogously, scientific programmers need to revise
publicly available (e.g. open source) projects and code that can be interesting for their
research. Therefore, you should try to learn as much as possible from your peers
and keep up-to-date with all the developments of
relevant projects. GitHub enables this functionality by _following_ other
GitHub users (see also Rule 2) or _watching_ the activity of projects, which is a common
feature in many social media platforms. Take advantage of it as much
as possible!

## Conclusions

If you are interested and have not used git and GitHub before, we
recommend you to get started as soon as possible. As with many other
tools, a certain learning curve lays ahead. However, basic yet very
useful features can be relatively easily learned and applied to many
different use-cases \cite{ram2013git}. We anticipate the reward will be worth your
effort. To conclude, we would like to recommend some examples of bioinformatics
repositories in GitHub (Table 1) and some useful training
materials including workshops, online courses and manuscripts (Table
2).


Table 1: Bioinformatics repository examples with good practices using GitHub. The table contains the name of the repository, the type of the 
example (issue tracking, branch structure, unit tests) and the URL of the example. 


| Name of the Repository                           | Type                                                | URL                                                                          |
|--------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------------------|
| Galaxy Project                                   | Community Project, Bioinformatics Repository        | https://github.com/galaxyproject/galaxy/                                     |
| Retinal wave data repository                     | Binary Data organized                               | https://github.com/sje30/waverepo/tree/master/hdf5                           |
| OpenMS                                           | Bioinformatics Repository, issue discussion         | https://github.com/OpenMS/OpenMS/issues/1095                                 |
| Pride Inspector Toolsuite                        | Project Organization, multiple project repositories | https://github.com/PRIDE-Toolsuite                                           |
| BioPython                                        | Community Project, multiple contributors            | https://github.com/biopython/biopython/graphs/contributors                   |
| Adam                                             | Community Project, Multiple forks                   | https://github.com/bigdatagenomics/adam/network                              |
| Computational Proteomics Unit                    | Lab Repository                                      | https://github.com/ComputationalProteomicsUnit/                              |


Table 2: Online courses, tutorials and workshops about GitHub and Git for scientist.

| Name of the material                             | Type                 | URL                                                                          |
|--------------------------------------------------|----------------------|------------------------------------------------------------------------------|
| `git help` and `git help -a`                     | Documentation        | Local, installed with `git`                                                  |
| Karl Broman's git/github guide                   | Short tutorial       | http://kbroman.org/github_tutorial/                                          |
| Version Control with GitVersion Control with Git | Tutorial             | http://swcarpentry.github.io/git-novice/                                     |
| Introduction to Git                              | Tutorial             | http://git-scm.com/book/ch1-3.html                                           |
| Github Training                                  | Courses and Training | https://training.github.com/                                                 |
| Github Guides                                    | Tutorial             | https://guides.github.com/                                                   |
| Good Resources for Learning Git and GitHub       | Tutorials Directory  | https://help.github.com/articles/good-resources-for-learning-git-and-github/ | 
| Software Carpentry: Version Control with Git     | Tutorial             | http://swcarpentry.github.io/git-novice/ |


 
## Disclaimer

The authors have no affiliation with GitHub, nor any commercial entity
mentioned in this article. The views described here reflect their own
without input from any third party organisation.

## References
