#Ten Simple Rules for taking advantage of GitHub in bioinformatics

Yasset Perez-Riverol *, Rui Wang, Timo Sachsenberg (2), Julian Uszkoreit (3), Laurent Gatto (4), Felipe da Veiga Leprevost (5),  Juan Antonio Vizcaíno *

1 European Molecular Biology Laboratory, European Bioinformatics Institute (EMBL-EBI), Wellcome Trust Genome Campus, Hinxton, Cambridge, CB10 1SD, UK.

(2) Applied Bioinformatics and Department of Computer Science, University of Tübingen, D-72074 Tübingen, Germany.

(3) Medizinisches Proteom-Center, Ruhr-Universität Bochum, Universitätsstr. 150, D-44801 Bochum, Germany

(4) Computational Proteomics Unit, Cambridge Systems Biology Centre,
University of Cambridge Tennis Court Road Cambridge, CB2 1GA, UK

(5) Department of Pathology, University of Michigan, Ann Arbor, Michigan 48109

* Corresponding author: Dr. Yasset Perez-Riverol
European Molecular Biology Laboratory, European Bioinformatics Institute (EMBL-EBI),
Wellcome Trust Genome Campus, Hinxton, Cambridge, CB10 1SD, UK. Tel:
+44 1223 492 610; Fax: +44 1223 494 484; Email: yperez@ebi.ac.uk.

* Corresponding author: Dr. Juan Antonio Vizcaíno European Molecular
Biology Laboratory, European Bioinformatics Institute (EMBL-EBI),
Wellcome Trust Genome Campus, Hinxton, Cambridge, CB10 1SD, UK. Tel:
+44 1223 492 610; Fax: +44 1223 494 484; Email: juan@ebi.ac.uk.


Short title: Ten Simple Rules for taking advantage of GitHub in
bioinformatics    

## Introduction

Bioinformatics is a broad discipline in which the common denominator is the need to produce and/or use software that can be applied to biological data in different contexts. For instance software is routinely needed for the analysis, visualization [PMID:25475079],
integration or storage of biological information. To enable and ensure the reproducibility of scientific claims, it is essential that,
together with the scientific publication, the corresponding dataset/s are made publicly available to the scientific community
[PMID:24763340,PMID:25158685]. In addition, all the software used for the analysis should be either well described (e.g. in case of using
commercial software) or openly shared, when possible [PMID:24675742,PMID:25993922]. At present the latter is becoming more
common in the case of "home made" programming scripts or for bioinformatics open-source projects, where the source code is made openly available and can be reused by third parties [PMID:25071829]. The open availability of the source code can be achieved thanks to the existence of several code repository-hosting services such as Sourceforge (http://sourceforge.net/), Bitbucket (https://bitbucket.org/) and GitHub (https://github.com/), among others.These resources are also essential for collaborative software projects, since they enable the organization and sharing of programming tasks between different contributors to the same project. Here we aim to introduce the main
features of GitHub, a popular web-based platform which offers a free and integrated environment for hosting the source code, documentation and web page for open source projects. A reason for GitHub's success is that it offers more than a simple source code hosting service. It provides developers with a dynamic and collaborative environment, often coined as social coding platform, with the ability to review, comment and discuss code [Social coding in GitHub: transparency and collaboration in an open software repository, ACM, 2012.]. In addition, third party extensions offer additional services to complete the development stack, including continuous integration and deployment of software. The cornerstone of GitHub is the well-known and open-source version control system git, designed and developed by Linus Torvalds in 2005 to control and extend the Linux kernel development. It has become the most widely adopted version control system, used by major companies such as Google, Facebook, or Twitter, among others.  GitHub is free to use for publicly available projects, therefore hosting millions of open source projects. In addition, it offers paid plans for private repositories. Some of the recommendations outlined below would be applicable to other hosting services as well. However our main aim here is to highlight specific GitHub features. We will then provide a set of recommendations for taking full advantage of its core features to facilitate and manage the work on a given bioinformatics project and increase its profile to the scientific community.


## Rule 1: Structure your projects: users, organizations, repositories, and teams

Open projects on GitHub are visible to everyone, but write permissions
to change the source code need to be granted. Structuring your
projects allows the management of permissions, restricting access at
different levels: users, teams and organizations. Users are the
keystone of GitHub, as for any other social network. Every user has a
profile listing their GitHub projects and activities which can be
optionally populated with personal information including name, e-mail
address, image and webpage. To stay up to date with the activity of
other users you can "follow" their accounts. Collaboration can be
achieved by simply adding a trusted "Collaborator" and thereby
granting write access. However, development in large projects is
usually done by several teams of people, within a larger
organization. GitHub organizations are a great way to manage
team-based access permissions for the individual projects of
institutes, research labs, and large open-source projects that need
multiple owners and administrators (Figure 1). For individual
researchers, we recommend that you make your profile visible to other
users and display all the projects and organizations you are working
on, including a list of the latest activities on the site (Comment:
here we can add a Figure 1 with major options of GitHub).  Finally,
repositories (the shorten term is "repo") are versioned directories or
dedicated storage space for your software projects. It can be included
inside your organization or can belong to particular users. Users can
usually keep code, text files, images and small data files inside a
repository. And while many users store programs and code projects,
there is nothing preventing you from keeping text documents or other
file types in your project [citation]. Note that until recently,
GitHub had a lack of support for storing large files (> 100 MB). This
has been recently addressed by the GitHub large file storage [cite].

##Rule 2: Learn Git and embrace its power

The cornerstone of GitHub is the distributed, version control system
Git. Every change, from fixing a typo to a complete redesign of the
software is controlled by versions, so called revisions
[JU: aren't these called commits??? actually, i just googled around: it seems to be used synonymously, but on github seems to be always called a commit]
[add citation]. While beginners may consider the learning curve of Git
steep, many detailed tutorials exist. If you are new to Git, you can
consider a revision as a "snapshot" (version) of a file system. Git is
remarkably effective in archiving the complete history of your project
(all revisions) by, amongst other things, storing only the differences
between the revisions. To create a new revision, the set of changes
(e.g. new, deleted or modified files) introduced are committed to the
repository. (Comment: perhaps here will be interested to add some
snippet code of a commit). Following the rule: "commit often, as most
as you can, perfection later", one can keep track of the development
in small incremental changes. At any time it is possible to go back to
a previous version. In larger projects, multiple users contribute to
the same repository. To manage concurrent developments with commits to
the same repository several approaches are commonly used. The most
common way is to use Git branches to separate different lines of
development. Active development is often performed on a development
branch and stable versions as e.g. used for a software release are
kept in a master branch. In practice, developers work on one or
several features or improvements. To keep commits of the different
features logically separated, distinct branches are typically used and
merged into the development line once they are finished. In projects
involving more than one contributor, everyone wants to be sure that
the contributions of others increase the quality and move the project
forward. This is especially the case if external contributors want to
incorporate e.g. a bug fix or novel feature without being a
collaborator or part of the same organization. Forking a repository
and providing pull-requests provide an easy way for collaboration
inside and over organizations boundaries. A user that forks a
repository creates a copy under his name. Modifications e.g. a branch
with few features or bug fixes can conveniently be provided to the
forked (upstream) repository by opening a pull-request. Once it is
opened for review and discussion, it usually results in additional
insights and in an increased code quality. Once a pull-request gets
accepted, typically it gets merged into the development branch. A good
practice of integrating the code in the master branch is for someone
else to merge your code into it, ensuring that at least two
contributors review each new change.

##Rule 3. Let others contribute and add ideas to your projects

GitHub issues are a great way to keep track of bugs, tasks, and
enhancements. Classical issue trackers are primarily intended to be
used as bug tracker. In contrast, GitHub's issues follow a different
philosophy: each tracker has its own section in every repository, and
can be used to trace bugs, new ideas, and enhancements, by using a
powerful but optional tagging system for each issue. Its main focus is
on collaboration, providing context by cross-references, and excellent
text formatting for each issue: (i) a title and description, (ii)
color-coded labels help you to categorize and filter issues, (iii)
milestone acts like a container for issues (e.g. weekly discussion
9/5-9/16 related with datasets), (iv) one assignee responsible for
working on the issue, and (v) comments that allow anyone with access
to the repository to provide feedback. Another aspect is its
simplicity. For instance, it does not require to fill out lengthy
forms including every information that might be valuable to reproduce
the bug. It only requires the user to give the title and provide some
optional text. If the developer is missing information he can simply
request it in a comment. GitHub issues are then more dynamic and pose
a lower barrier for users to report bugs and request features. A
well-organized and tagged issue tracker will help upcoming
contributors and users to understand the project more deeply.

## Rule 4: The code must be always ready to use: Make use of tests, deployments and continuous integration

The first rule of software development, especially in agile software development, is that the code needs to be ready to use as soon as
possible [PMID: 25071829, http://arxiv.org/abs/1311.7011], including its main functionality (e.g. free of bugs), and should be
well-documented and tested. In 2005, Martin Fowler defined the basic principles for continuous integration in software development
[Comment: Fowler, Martin, and Matthew Foemmel. "Continuous integration." Thought-Works http://www.thoughtworks.com/Continuous
Integration. pdf (2006)]. These principles have become the main reference for continuous integration best practices, and provide the framework needed to deploy software, and in some way also data. Every repository, script, mathematical model, and function should contain a set of self-automated tests. A source code may run, but that does not mean it is doing the right thing. The simple use of those self-automated tests is to detect possible bugs introduced by new features, or changes in the code or dependencies, but also to detect wrong results, the so called "logic errors", where the source code produces a different result compared to what you intended it to do. Then, continuous integration provides the way of automatically run all of these tests in the repository by checking data and software dependencies. To do continuous integration automatically GitHub has been integrated with other systems such as Travis (https://travis-ci.org), a hosted continued integration platform that is free to all open-source projects hosted on GitHub. These builds/deployments are triggered automatically when developers commit their code. Continues integration via Travis notifications, allows the team and contributors to know if the new changes work and prevent the introduction of errors in the code, making the repo always ready to use. To automatically perform testing and report, how well the testing coverage of the project is, Codecov (https://codecov.io) can be employed. This allows you to easily check, which parts of your code are already, and which ones are in need of tests.

## Rule 5. Make use of the self-hosted documentation, blogging and manuals, using markdown and GitHub web pages

Providing comprehensive documentation helps others to understand, and contribute back to your project. A strong system aimed at serving documentation can make life easier for the team and boost the productivity and visibility of the organization. GitHub Pages are "simple-looking" landing page that GitHub hosts for free without the need to provide a server side or database. GitHub users can create and host blog websites, help pages, manuals, tutorials and websites related to specific projects. "Pages" lets you do the same things as GitHub, but a preformatted name is needed for the repository. In addition, all the pages need to be in static HTML or Markdown format. Furthermore, Pages comes with a powerful static site generator called Jekyll (https://jekyllrb.com) that can be integrated with other platforms such as Bootstrap (http://getbootstrap.com/) or Disqus (https://disqus.com/).

## Rule 6. Make your code easily citable by others in publications

In research, it is always a good practice to ensure permanent and unambiguous identifiers for citable items like articles, proteins,
genes, metabolites, or datasets, among others. Digital Object Identifiers (DOIs) have been used for many years as unique and unambiguous identifiers for enabling the citation of scientific publications. More recently, a trend has started to produce DOIs for other types of scientific outputs such as biological datasets [PMID:24727771] or training materials. The main motivation behind this is to give scientists a better credit for their work [PMID:19587644], enabling at the same time a better way to cite and track it. A common issue with software presented through scientific papers is that the sofware normaly evolves in a different speed than papers can are published, this means that it's common to find a software with several new features and functionalities not described in the respective publication, but not as inovative as necessary to become another independent publication. If someone chooses this software for this new features, not
described in the paper, the citation will reference a paper that do not describe its full functionalities. Following this trend, GitHub now enables the use of DOIs to cite the code deposited, using the data archiving tool Zenodo (https://zenodo.org/). The procedure is simple and it is explained in detail here (https://guides.GitHub.com/activities/citable-code/). By default, Zenodo takes an archive of your repository each time you create a new release on GitHub. Before Zenodo can issue a DOI for your repository, you will need to provide some metadata information about the archived repository. Once the DOI has been assigned, apart from using it in your CV, you can add it to literature information resources such as Europe PubMed Central [PMID:25378340].

## Rule 7. Always link and highlight your deposited source code in publications

As already mentioned in the introduction, reproducibility of scientific claims should be enabled by providing openly the software and the datasets that are used in a particular study. You should always highlight as much as possible in your publications that your code is freely available in GitHub, together with any other relevant piece of information that you may have deposited. In our experience, this openness definitely increases your chances of getting the paper accepted for publication. On one hand, journal editors and reviewers have the opportunity to reproduce your findings during the manuscript review process increasing confidence in your results. On the other, once the paper is published, your work can be reproduced by any member of the scientific community, which can increase your citations and foster opportunities for further discussion and collaboration. Also have in mind that a public repository with available source code does not make the software open-source, it's the licensing that does. When creating a new repository it's imperative to choose a licese for your code, it's by the license terms that other people will know how to use ans share you code.

## Rule 8. Promote your project/s in the scientific community

In rule 5 we mentioned the possibility to generate blog posts and run a blog using the GitHub framework. In addition, GitHub also provides mechanisms for real-time communication. Gitter (http://gitter.im) is a GitHub-based chat tool, in limited beta at the time of writing, which enables developers and users to share aspects of their work. Gitter inherits the shape of the social groups operating around GitHub repositories, organizations, and issues. It relies on the identity within GitHub, creating IRC-like chat rooms for public and private repositories. From within a Gitter chat, members can reference issues, comments, or pull-requests. A different service is Gist (https://gist.github.com), which represents a unique way to share "code snippets", single files, parts of files, or full applications. Gist can work in two ways: public gists, that can be browsed and searched, and secret gists that are not provided through "Discover" (https://gist.github.com/discover). One of the main features of Gist is the possibility to embed code snippets in other applications, enabling users to embed a gist in any text field that supports JavaScript.

## Rule 9. Demonstrate your work experience, improve your CV

To move ahead in your scientific career or simply to find a new job, it is very convenient to show and demonstrate that you have
contributed to a given project and at which level. In GitHub it is easy to show the level of contribution of individuals to a particular
code base. It is then possible for third parties to appreciate whether one given person has been one of the main contributors or has only
done sporadic contributions, or to which projects someone is contributing in a regular basis. This can be very useful information
for e.g. a prospective employer. Another complementary way to build up your CV is to use GitHub to contribute to the increasingly used
"altmetrics" methods to capture the impact of your work. In scientific publishing, altmetrics are defined as non-traditional metrics that
have been proposed as an alternative the traditional citation impact metrics [23538811;25423184]. Altmetrics cover not just citation
counts, but also other aspects of the impact of a work, such as how many data and knowledge bases refer to it, article views, downloads,
or mentions in social and news media. One way to achieve this is to use the service "ImpactStory" (http://www.impactstory.org/). ImpactStory is an open source, non-profit organizations which provides web-based tools that provide altmetrics for blog posts, datasets, reviewer activity and software, among others. Users can link their ImpactStory profile to their GitHub account, displaying information such as the popularity of the project, or the number of forks (repository copies) that other people have made of your code. At present, ImpactStory is a subscription-based service. However, users can try the service for free for 30 days.

## Rule 10. Check periodically existing open source projects

One of the jobs of a scientist is to read routinely the published literature available. Analogously, one of the jobs of a scientific
programmer should be to revise publicly available projects and code that can be interesting for his/her research fields. You should try to learn as much as possible from your peers and colleagues and be updated with all the developments of a project you are interested
in. GitHub enables this functionality, which is already common in widely used social media platforms such as Facebook or LinkedIn. Take
advantage of it as much as possible!

## Conclusions

If you are interested and have not used GitHub so far, we recommend you to get started as soon as possible. As in any other topics, a learning curve is required for beginners. However, we anticipate the reward will be worth your effort.

## Acknowledgements

Y.P.R is supported by the BBSRC ‘PROCESS’ grant [reference
BB/K01997X/1] and by the BBSRC ‘Quantitative Proteomics’ grant
[reference BB/I00095X/1]. R.W. is also funded by grant
BB/I00095X/1. J.A.V. is supported by the Wellcome Trust [grant number
WT101477MA]. J.U. and T.S. are funded by the BMBF grant de.NBI -
German Network for Bioinformatics Infrastructure (FKZ031 A 534A). LG
is supported by the BBSRC Strategic Longer and Larger grant (Award
BB/L002817/1).

##References
 
