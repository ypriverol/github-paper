#Ten Simple Rules for taking advantage of GitHub in bioinformatics

Yasset Perez-Riverol, Rui Wang, Timo Sachsenberg, Laurent Gatto, Juan Antonio Vizcaíno,*

1 European Molecular Biology Laboratory, European Bioinformatics Institute (EMBL-EBI), Wellcome Trust Genome Campus, Hinxton,
Cambridge, CB10 1SD, UK.


* Corresponding author: Dr. Juan Antonio Vizcaíno European Molecular Biology Laboratory, European Bioinformatics Institute
(EMBL-EBI), Wellcome Trust Genome Campus, Hinxton, Cambridge, CB10 1SD, UK. Tel: +44 1223 492 610; Fax: +44 1223 494 484; Email:
juan@ebi.ac.uk.


Short title: Ten Simple Rules for taking advantage of GitHub in bioinformatics


 
##Introduction

Bioinformatics is a broad discipline in which the common denominator is the need to produce and/or use software that can be
applied to biological data in different contexts. For instance software is routinely needed for the analysis, visualization
[PMID:25475079] or storage of biological information. For enabling and ensuring the reproducibility of scientific claims, it is
essential that, together with the scientific publication, the corresponding dataset/s are made publicly available to the
scientific community [PMID:24763340,PMID:25158685]. In addition, all the software used for the analysis should be either well
described (e.g. in case of commercial software) or openly shared, when possible [PMID:24675742,PMID:25993922]. At present the
latter is becoming more common in the case of “home made” programming scripts or for bioinformatics open-source projects, where
the source code is made freely available and can be reused by third parties [PMID:25071829]. The availability of the source code
can be achieved thanks to the existence of several code repository-hosting services such as Sourceforge (http://sourceforge.net/),
Bitbucket (https://bitbucket.org/), Google Code (https://code.google.com/) and GitHub (https://GitHub.com/), among others. These resources are also essential for
collaborative software projects, since they enable the organization and sharing of programming tasks between different
contributors to the same project.

Here we aim to introduce the main features of GitHub and related tools and services, as a web-based platform, which offers a free and integrated environment for hosting the source code, the documentation and the web page of open source projects.But there is more to it than a merge sourcecode hosting service. GitHub offers developers a dynamic and collaborative environment often coined as social coding platform with the ability to review and comment code [add citation]. In addition, third party extensions offer additional services to complete the development stack, including continuous integration and deployment of software. While small projects usually start with small scripts and little code, it is the ability to scale from single developer efforts to large projects with hundreds of developers. The cornerstone of GitHub is the well-known and
open-source version control system Git, designed and developed by Linus Torvals in 2005 to control and extend the Linux kernel
development; and has become the most widely adopted version control system; adopted by major companies like Google, Facebook,
Twitter. GitHub is free to use for use for public projects and offers paid plans for private repositories, and it is the host of
millions of open source projects. We will provide a set of recommendations for taking full advantage of the core features of
GitHub to facilitate and manage the work on a given bioinformatics project and increase its profile to the scientific community.
The manuscript is timely due to the announcement of the closure of another widely used service, Google Code. Therefore, many of
the users of Google Code will therefore migrate to GitHub in the coming months. Rules

##Rule 1: Structure your research projects: users, organization, repositories, and teams

Free projects on github are visible to everyone, but write permissions need to be granted. Structuring your projects allow to manage permissions and restrict access on different levels: users, teams and organisations. Users are the keystone of GitHub; as for any other social network. Every user has a profile listing their GitHub projects and activities which can be optionally populated with personal information including name, email address, image and webpage. To stay up to date with other users you simply connect by “following” their accounts. Collaboration on e.g. your single user projects can be achieved by simply adding a trusted “Collaborator” and thereby granting write access. However, development in large projects is usually done by several teams of people, within a larger organization. GitHub organizations are a great way to manage team-based access permissions for the individual projects of institutes, research labs, and large open-source projects that need multiple owners and administrators (Figure 1).
For researcher, we recommend that you make your profile visible to other users and displays all the projects and organizations you are working on and a list of their latest activities on the site (Comment: here we can add a Figure 1 with major options of GitHub). 
Repositories (shorten term “repo”) are versioned directories or storage space of your software or research projects. It can be included inside you organization or can belong to particular users. Users usually keep code files, text files, image files and small data files, inside a repository. And while many users store programs and code projects, there’s nothing preventing you from keeping text documents or other file types in your project making GitHub and excellent service and platform for bioinformatics and open-source research [citation]. Note that until recently, GitHub had a lack of support for storing large files (> 100mb). This has been recently addressed by the github large file storage [cite].

##Rule 2: Learn git and embrace its power

The cornerstone of GitHub is the distributed, version control system Git. Every change, from fixing a typo to a complete redesign
of the software is controlled by versions, so called revisions [add citation]. While beginners may consider the learning curve of Git steep, many step by step tutorials targeted to beginners exist. If you are new to Git, you can think about a revision as a “snapshot” (version) of a filesystem. Git is remarkably effective in archiving the complete history of your project (all revision) by, amongst other things, storing only differences between revisions. To create a new revision, the set of changes (e.g. new, deleted or modified files) introduced are commited to the repository. (Comment: perhaps here will be interested to add some snippet code of a commit). Following the rule: “commit often, as most as you can; perfection later”; one can keep track of the development in small incremental changes. At any time going back to a previous version is possible.
In larger projects, multiple users contribute to the same repository. To manage conccurent developments with commits to the same repository several approaches are commonly used. The most common way is to use git branches to separate different lines of development. Active development is often performed on a develop branch and stable versions as e.g. used for a software release are kept in a master branch. In practice, developers work on one ore several features or improvements. To keep commits of the different features logically separated, distinct branches are typically used and merged into the development line once they are finished.
In projects involving more than one contributor, everyone wants to be sure than the contributions of others
increase the quality and move the project forward. This is especially the case if external contributors want to incorporate a e.g. bug fix or novel feature without beeing a collaborator or part of the same organization.
Forking a repository and providing Pull-Requests provide an easy way for collaboration in and over organizations boundaries. 
A user that forks a repository creates a copy under his name. Modifications e.g. a branch with few features or bug fixes can conveniently be provided to the forked (upstream) repository by opening a Pull-Request. Once a Pull-Request has been opened, it is open for review and discussion usually resulting in additional insights and increased code quality. Once a Pull-Request gets accepted, it gets typically merged into the development branch. A good practice of integrating the code in the
master branch is for someone else to merge your code into it, ensuring that at least two contributors review each feature, data, file or new change. Every small change in large/collaborative project should be done by pull-request boosting the quality of the project and its data.

##Rule 3. Let’s others contribute and add ideas to your projects.

GitHub issues are a great way to keep track of bugs, tasks, and enhancements for your projects. Classical issue tracker are primarily intended to be used as bug tracker of
projects. In contrast, GitHub’s issues follow a different philosophy: each tracker has its own section in every repository, and can be use to trace bugs, new ideas, enhancements
by using a powerful but optional tagging system of each issue. Its main focus is on collaboration,
providing context by cross-references, and excellent text formatting by using for each issue: (i) a title and description, (ii) color-coded labels help you
categorize and filter your issues, (iii) milestone acts like a container for issues (e.g. weekly discussion 9/5-9/16 related with
datasets), (iv) one assignee responsable for working on the issue, and (v) comments that allows anyone with access to the
repository to provide feedback related with the issue. Another aspect is its minimalisticity. For instance, it does not require to fill out lengthy forms including every information that might be valuable for the developer to reproduce the bug. It only requires the user to give the title and and optional text. If the developer is missing information he simply requests them in a comment. In this regards, GitHub issues are more dynamic and pose a lower barrier for users to report bugs and request features. A well-organized and tagged issue tracker will help upcoming
contributors and users to understand the project more deeply. The issue tracker tells the story of the repository/project where
new users can learn the reasons behind decisions and contributors can discuss the progress of the project.

##Rule 4: Always ready to use: Tests, Deployments and Continuous integration 

The first rule of software development, especially in agile software development, is that the code needs to be ready as soon as
possible [PMID: 25071829, http://arxiv.org/abs/1311.7011]; including main functionalities free of bugs, well-documented and
tested. In 2005, Martin Fowler defined the basic principals for continue integration in software development (Comment: Fowler,
Martin, and Matthew Foemmel. "Continuous integration." Thought-Works) http://www. thoughtworks. com/Continuous Integration. pdf
(2006)). These principles have become “THE” set of Continuous Integration best practices, and provide the framework about how to
deploy software and in some way data. Every repository, scripts, mathematical model, function should contains a set of
self-automated tests; a source code my run, but that doesn't mean it does the right thing. The simple use of those self-automated
tests is to detect possible bugs introduced by new features, or changes in the code or dependencies, but also detect wrong results
or so called “logic errors” where your source code produce a different results compare with what you intended it to do [add
citation]. Then, continues integration provides the way of automatically run all of these tests in the repository by checking
dependencies, data, and environment dependencies. To do Continuous Integration automatically GitHub has been integrated with other
systems such as Travis (https://travis-ci.org), a hosted continued integration platform that is free to all open-source projects
hosted on GitHub. These builds/deployments are triggered automatically when each developer checks/commits their code/data to the
repository. Continues integration via Travis notifications, allows the final team and contributors to know if the new changes work
and do not introduce any error in the repository, making the repo always ready to be use.


The first rule of software development and special in agile software development, is that the code needs to be ready as soon as
the project starts [PMID: 25071829]. Especially, the first prototype of the software including main functionalities should be
avaible as soon as possible free of bugs, well-documented and tested.

##Rule 5. Self-Hosted documentation, blogging and manuals using markdown and GitHub web-pages

Providing well-written documentation helps others understand, and contribute back to your project. A strong system
used to serve documentation can make life easier for the team writing it and boost the productivity and visibility of the
organization. The difficult step about documentation should be which specific test we will include, which examples are the most
clear for the users; not configuring tools or figuring out how to deploy updates. GitHub Pages are “simple-looking” websites that
GitHub hosts for free without needs to provide a server side, database, etc. GitHub users can create and host both blogs websites,
help pages; manuals, tutorials and websites related to specific GitHub projects. Pages lets you do the same things as GitHub, but
a preformatted name is need for the repository; and all the pages needs to be HTML or Markdown. Also, Pages comes with a powerful
static site generator called Jekyll (https://jekyllrb.com) that can be integrated with other platforms such as Bootstrap
(http://getbootstrap.com/) or Disqus (https://disqus.com/).

##Rule 6. Make your code easily citable by others in publications

In research, it is always a good practise ensure permanent and unambiguous identifiers for citable items like articles, proteins, genes, metabolites, or datasets, among many other items. Digital Object Identifiers (DOIs) have been used for many years as unique and unambiguous identifiers for enabling the citation of scientific publications. More recently, a trend has started to produce DOIs for other types of scientific outputs such as biological datasets [PMID:24727771] or training materials. The main motivation behind is to give scientists a better credit for their work [PMID:19587644], enabling at the same time a better way to cite and track it. Following this trend, GitHub now enables the use of DOIs to cite the code deposited, using the data archiving tool Zenodo (https://zenodo.org/). The procedure is very simple and it is explained in detail here (https://guides.GitHub.com/activities/citable-code/). By default, Zenodo takes an archive of your GitHub repository each time you create a new release on GitHub. Before Zenodo can issue a DOI for your repository, you will need to provide some metadata information about the archived GitHub repository. Once the DOI has been assigned, apart from using it in your CV or add it to information resources such as Europe PubMed Central [PMID:25378340].


##Rule 7. Always link and highlight your deposited source code in publications 

As already mentioned in the introduction, reproducibility of the scientific claims should be enabled by providing openly the
software and the datasets that are used in a particular study described in a publication. You should always highlight as much as
possible in your publications that your code is freely available in GitHub, together with any other relevant piece of information
that you may have deposited. In our experience, this openness definitely increases your chances of getting the paper accepted for
publication. On one hand, journal editors and reviewers have the opportunity to reproduce your findings during the manuscript
review process increasing confidence in your results. On the other, once the paper is published, the same can be done by any
member of the scientific community, which can increase your citations and foster opportunities for further discussion and collaboration.

##Rule 8. Promote your project/s in the scientific community

In rule 5 we mentioned the possibility to generate your blog posts and run a blog around your repository or organization using the GitHub framework. But GitHub, has more for its users, by providing mechanisms for real-time communication. Gitter (http://gitter.im) is a GitHub-based chat tool, now in limited beta, which allows the developers and users to chat about repositories/code and organizations. Gitter inherits the shape of the social groups operating around GitHub repositories, organizations, and issues; and relies on the social identity within GitHub, creating IRC-like chat rooms for public and private repositories. From within a Gitter chat, members can reference issues, comments, pull-requests, etc. 
Also, Gists (https://gist.github.com) are a unique way to share your “code snippets”, single files, parts of files, or full applications. Gist has to types of gists: public gist that can be browseable and searchable; and secrets that are not provide through Discover (https://gist.github.com/discover). One of the main feature of gist is the possibility to embed code snippeds in other applications. The user can embed a gist in any text field that supports Javascript, such as a blog post, documentation page or web. 



##Rule 9. Connecting the other dots
To move ahead in your scientific career or simply to find a new job, it is very convenient to show and demonstrate that you have
contributed to a given project and at which level. In GitHub it is easy to show the level of contribution of individuals to a
particular code base. It is then possible for third parties to appreciate whether one given person has been one of the main
contributors or does only sporadic contributions, or to which projects someone is contributing in a regular basis. This can be
very useful information for a prospective employer. Another complementary way to build up your CV is to use GitHub to contribute
to the increasingly used “altmetrics” methods to capture the impact of your work. In scientific publishing, altmetrics are defined
as non-traditional metrics that have been proposed as an alternative the traditional citation impact metrics [23538811;25423184].
Altmetrics cover not just citation counts, but also other aspects of the impact of a work, such as how many data and knowledge
bases refer to it, article views, downloads, or mentions in social and news media. One way to achieve this is to use the service
“ImpactStory” (http://www.impactstory.org/). ImpactStory is an open source, non-profit organisation that provides web-based tool
that provides altmetrics for blog posts, datasets, reviewer activity and software, among others. Users can link their ImpactStory
profile to their GitHub account, displaying information such as the popularity of the project, or the number of forks (repository
copies) that other people have made of your code. At present, ImpactStory is a subscription-based service. However, users can try
the service for free for 30 days.


##Rule 10. Be social: Discover the power of open source projects and contribute to others

One of the jobs of a scientist is to read routinely the published literature available. Analogously, one of the jobs of
programmers should be revise publicly available projects and code that can be interesting for his/her interests. GitHub makes this
possible.

You should try to learn as much as possible from your peers and colleagues and be updated with the developments of a project you
are interested in. GitHub enables functionality that is already common is commonly used Social Media platforms such as Facebook or
LinkedIn.



##Conclusions
To summarize, you can benefit for using GitHub in many different ways.



##Acknowledgements
Y.P.R is supported by the BBSRC ‘PROCESS’ grant [reference BB/K01997X/1] and by the BBSRC ‘Quantitative Proteomics’
grant [reference BB/I00095X/1]. J.A.V. is supported by the Wellcome Trust [grant number WT101477MA].



 



