# Reviewer 1

The authors provide a fairly comprehensive overview of how to use
GitHub for scientific computing projects, with some specifics about
bioinformatics.
 
First, let me say that I am a huge fan of git and github, and have no
complaints about the overall message. My only concern is to help the
authors deliver an effective argument!

That having been said, I find the organization and discussion of this
paper to be confusing and to do a somewhat poor job of "selling"
github. The discussions are overcomplicated and read like a wall of
text, rather than making clear, specific points.

For example, "Rule 1".

- the title makes no sense if you don't already know something about github.
- I'm not sure what the main message is intended to be - there are several
currently - but I like the sentence starting with "Github organisations
are a great way". Perhaps "GitHub can be used for collaboration"?
- but that might be a bad introduction. Why not, "you should be using git
in the first place" (rule 2) as rule 1?

I have many similar comments about the 

I think the authors should take a step back and simplify their 10 main
messages, and then write around that. Here is an example (not well
thought out) --

Rule 1: Use GitHub to track your lab and personal proejcts.
Rule N: Use GitHub to deliver and maintain versions of your code.
Rule N: Use GitHub to advertise your project. (can include web site)
rule N: Use GitHub to track issues reported by users.
Rule N: GitHub integrated services can do lots of nice things (CI).

I am happy to provide more detailed critiques but I think the overall
organization is getting in the way of the message.

I would also urge the authors to post this as a preprint and get some
discussion of it going in public[*]. There are lots of academics using
github and you will get quite a bit of helpful advice.

[*] perhaps you could use github to do this? :)

## Meso comments:

Plans that provide some private repositories are free for academic users
of github. This is one of the major concerns of adoption; might be worth
highlighting. (I think everything should be open, but that's a hard message
to swallow.)

Github large file support is not free, generally speaking.

> R/ We added a new sentence to the introduction highlighting this concern.

In the conclusions, the (substantial) learning curve of git is
mentioned. Perhaps some pointers to open lessons should be made
available, along with workshops? For example, both Data Carpentry and
Software Carpentry teach git and github on a global basis.
(Disclaimer: I am heavily involved with both.)

> R/ We agree with the reviewer and in the present version we added some useful links to 
documentation, coursers and tutorials. 

## Minor comments:

It could be made clearer that all files involved in a change are made
part of a single revision.

Gitter is not owned by github, AFAIK. They just integrate. (Line 203).
Why prioritize it over others? For example, Slack is another service
that provides similar functionality. (We use gitter, but still.)

> R/ We agree with the reviewer. In the present version we refined the paragraph making clear 
that Gitter is not only chat system integrated with Github. We also included Gitter as an example of 
chat system but leaving the space open for other systems.   

Rule 10 title should be "Periodically check..."

> R/ We agree with the reviewer and the current version was changed.

missing reference:
http://scfbm.biomedcentral.com/articles/10.1186/1751-0473-8-7

Signed,

C. Titus Brown
ctbrown@ucdavis.edu


# Reviewer 2

This paper provides valuable orientation to modern 'best practices'
for nascent developers of bioinformatic software. The manuscript will
appeal to an important part of the bioinformatics community, and will
help many individuals take the 'next step' in solidifying their
overall contribution.

1. Reproducibility should not be mentioned (in the introduction) as a
   motivating factor. Having available software is of course a
   necessary condition, but in reality the temporal scale (years after
   the original analysis) and complexity (operating systems,
   compilers, libraries, software ecosystem, ...) of analyses really
   mean that the individual investigator interested in reproducible
   research MUST take charge of the situation at the time of the
   original analysis, and cannot rely on availability of versioned
   software after the fact.
   
> R/ we replaced the word reproducibility by two different terms replicability and traceability. The current version of
  the manuscript explain:
  
> To enable and ensure the replicability and traceability of scientific claims, it is essential that the scientific publication,
  the corresponding datasets and the data analysis are made publicly available \cite{Goodman:2014,Perez-Riverol:2015}

2. It would be very helpful to call out, with links to repository
   locations, exemplar github repositories of individual developers
   (from among the authors?), labs (from the authors, or from
   successful projects / groups like bedtools, Lior Pachter's lab?),
   intermediate projects (hts / samtools?), and larger projects
   (rOpenSci??) that effectively use GitHub.
   
> R/ Thanks for this comment. We just added a couple of repositories in the introduction. The current version of the manuscript:

> Individual bioinformatics projects (https://github.com/lgatto/MSnbase) \cite{Gatto15012012}, 
  lab repositories (https://github.com/PRIDE-Toolsuite/) \cite{Perez-Riverol01012016}, intermediate projects such as (https://github.com/samtools) and 
  OpenMS (https://github.com/OpenMS) \cite{sturm2008openms}; or global collaborations such as ROpenSci (https://github.com/ropensci) 
  and The Global Allience For Genomics and Health (https://github.com/ga4gh) has found the perfect place in GitHub to share code, ideas and collaborate.


3. Of course the emphasis on GitHub is challenging. We know that this
   service cannot be indefinite, just as Sourceforge, Google Code,
   etc., have all faded. The manuscript should emphasize principles as
   much as possible, rather than the GitHub realization of those
   principles; I realize that GitHub does a great job of bringing
   bioinformatics developers into the modern age. Minimally, I think
   that Git and GitHub should be removed from the title and all
   'Rules' headers.
   
> R/ We partially agree with the reviewer. In the current version of the manuscript we remove from some of the rules (the ones that explain concepts) the GitHub 
term. However, some of the rules are focus on the functionalities provided by Git, in those cases we keep the term in the title for example **Rule 2**. Git as a protocol is 
used by different services such as GitHub, Bitbucket. For that reason we will keep the Git term in **Rule 2** because we would like to highligth the power of git compare with 
other version control systems. In the current version we removed the term from **Rule 7** making possible to highligth the concept rather than the service.  

4. The merits of individual recommendations should be reinforced with
   links to relevant examples, e.g., of an open issue, relevant
   commentary, and appropriate resolution. Similarly oriented links
   would help to convey the value / ease of continuous integration,
   and of test coverage.
   
>R/ We agree with the reviewer. In the present version of the manuscript we included examples
 in most of the sections of the manuscript.

5. The target audience is the relatively 'novice' developer; more
   established researchers will have their own procedures in place,
   will be aware of the current state-of-the-art, or will be too stuck
   in their ways to benefit from the discussion. From this
   perspective, it seems counter-productive to include 'organizations'
   and even 'teams' in rule 1; really one wants to get the individual
   or at most the individual + lab group oriented; 'organizations'
   (including the GitHub concept) are not immediately relevant.
   
> R/ We undestand the reviewer point. However, we think we should explain most of the features and best practices 
 of using github. We added different examples about how to use the different components of github and to explain in a 
 better way every github/git concept.

6. Rule 3 should be refined to emphasize that branches are really
   short-term departures from master; it is too easy for academic
   developers to lose track of the thrust of their project, or for
   individuals to work in isolation for extended periods, so that
   their contribution cannot easily be merged back to master.
   
> We agree with the reviewer. The current version of **Rule 3** emphasize the use of branches as short-term departures from master: 

> One of the easiest ways to make a mess for yourself with Git is to allow your _branch_ to get
  out of sync. Branches are just short-term departures from master. If you
  pull frequently, you will keep your copy of the repo up to date, and you will
  have the opportunity to merge your changed code with others' contributors.

7. Rule 5 should be clarified. It includes really two points. The
   first is the use of unit tests to ensure that the software is doing
   as advertised. The second is the practice of committing (to master)
   running code. Maybe it would be better to break these out, and go
   for the novelty of 11, rather than the familiar 10, rules.
   
> We refined the **Rule 5** and it only provides information about unit test 
and the idea of continues integration.

8. In Rule 5 and in the context of unit tests (and also in the
   'automatic' generation of documentation), I think that many
   attempts at unit tests / documentation are superficial and
   misguided. At least from an anecdotal perspective, I'm sure we all
   are familiar with the information-less javadoc along the lines of
   'field foo is an integer that defines foo'. Certainly unit tests
   that validate inputs and even outputs are valuable. But somehow one
   would like to elevate unit tests of scientific software to the
   'next level', where the assertions of the mathematical closure
   implied by the unique analytic methods are evaluated, rather than
   merely the correctness of the inputs; one would like to do this in
   the spirit of unit, rather than integration, tests, and metrics
   like code coverage are imperfect at capturing this. Likewise I
   think attempts to 'automatically update the documentation on code
   modification' are almost counter-productive -- availability of this
   level of documentation is not really what users crave.
   
> R/ We leave the Rule 5 about unit tests and redefine the 

9. Rule 9 does not mention the obvious, effective, and esssential
   method for promoting one's project -- publishing in the
   peer-reviewed scientific literature!
   
> We agree with the reviewer. The current version of the rule starts by making clear this statement:

> The traditional and effective way of promoting scientific software is by
  publishing them in the peer-reviewed scientific literature.

# Reviewer 3

I recommend the manuscript 'Ten Simple Rules for Taking Advantage of GitHub in
Bioinformatics' by Perez-Rivero et al should be accepted pending minor revisions
(see below).  The work on the paper isn't novel (lots of related articles and
guides for source code repos for life scientists) but this fits well within the
educational 'Ten Simple Rules' articles, and is a nice and pertinent
summarization of the key features of GitHub and specific use cases for scientists.

## Comments:

1. Small thing: I would suggest a minor title change to reflect that
   (even though this *is* going into PLOS CompBio) that the rules
   aren't just specific to bioinformatics. In fact, the term
   'bioinformatics' appears exactly exactly twice in the paper
   (leaving out the title and affiliations), both times in the
   'Introduction' text!  Beyond that, one could substitute any
   discipline for 'bioinformatics' as long as it required some need
   for version control. Maybe something like "Ten Simple Rules for
   Taking Advantage of GitHub for Scientists".  I'm horrible with
   titles, though, maybe I shouldn't come up with this :)
   
> We agree with the reviewer. The present version of the mansucript has a different title:

> Ten Simple Rules for taking advantage of GitHub

2. Pg. 1, Introduction, para1: "Here, we introduce the main features
   of GitHub, a popular web-based 14 platform which offers a free and
   integrated environment for hosting the source code, documentation
   and web page for open source projects."

   Probably a better way to word ‘web page’, something like ‘public
   project-related web content’ since many projects are more complex.
  
> We agree with the reviewer an in the present version we included a small change:

> Here, we introduce the main features of GitHub, a popular web-based platform
  which offers a free and integrated environment for hosting the source
  code, documentation and project-related web content for open source projects. GitHub also
  offers paid plans for private repositories. 

3. Pg. 2, Introduction, para 2: small revision suggestion 

   “These rules have been ordered to reflect a typical development
   process: learning git and GitHub basics, use of branches, labeling
   and tagging of code snapshots, tracking project bugs and
   enhancements using issues, etc”

4. Pg. 2, Rule 1:

    a) Might be worth explaining what 'forking' means.
    
> We agree with the user and the current version include a short explanation of the forking concept. 

    b) "Structuring your projects allows to manage permissions and restrict
    access at different levels: users, teams and organisations."  Maybe "Project
    managers can structure projects to manage…"

> We agree with the reviewer and the current version include the suggested change.

    c) Repositories: The bit on repositories should be described earlier, not at
    the end.  You are technically forking a *repository*, not just a project
    (which in my opinion could consist of many independent but related
    repositories, e.g. the Bio* projects, GMOD, etc).
    
> We re-structured the rule and the current version started explaining what is a repository. 

5. Pg. 3, Rule 2:

    a) "The cornerstone of GitHub is the distributed version control system git.
    Every change, from fixing a typo to a complete redesign of the software, is
    controlled by versions, so-called revisions." (added a comma after
    'software')
    
> We changed the sentence in the present version. 

6. Pg. 3, Rule 3:

    a) "Nevertheless, one can always pull the currently up-to date master branch
    into one branch, enabling one to react or adapt to the changes in the stable
    code branch." (use 'branch', not 'fork')
    
>  We changed the sentence.

    b) "Once a pull request is opened for review and discussion, it usually
    results in additional insights and increased code quality" ('it' was
    ambiguous)

7. Pg. 5, Rule 8:

    a) "The main motivation behind this is to give scientists a better credit
    for their work".  True, but this is also key for grants and funding, where
    many funding agencies such as NIH now accept other 'products' of research as
    citable research (these being publicly accessible data and software).
    
> We agree with the reviewer. The present version mentioned also funding agencies.

> In addition, funding agencies such as NIH now accept other research products as citable research such as accessible datasets and softwares.

    b) https://guides.github.com/activities/citable-code/
    Should be consistent w/ other URLs in text
    
> We changed the current version.

    c) ‘On one hand… on the other hand’ usually are used to describe two sides
    or opposing viewpoints. Not sure it’s used correctly here, since both
    examples are complementary, not in opposition to one another?
    
> We agree with the user and the present version reflects the reviewer comments.  

Chris Fields
