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

In the conclusions, the (substantial) learning curve of git is
mentioned. Perhaps some pointers to open lessons should be made
available, along with workshops? For example, both Data Carpentry and
Software Carpentry teach git and github on a global basis.
(Disclaimer: I am heavily involved with both.)

## Minor comments:

It could be made clearer that all files involved in a change are made
part of a single revision.

Gitter is not owned by github, AFAIK. They just integrate. (Line 203).
Why prioritize it over others? For example, Slack is another service
that provides similar functionality. (We use gitter, but still.)

Rule 10 title should be "Periodically check..."

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

2. It would be very helpful to call out, with links to repository
   locations, exemplar github repositories of individual developers
   (from among the authors?), labs (from the authors, or from
   successful projects / groups like bedtools, Lior Pachter's lab?),
   intermediate projects (hts / samtools?), and larger projects
   (rOpenSci??) that effectively use GitHub.

3. Of course the emphasis on GitHub is challenging. We know that this
   service cannot be indefinite, just as Sourceforge, Google Code,
   etc., have all faded. The manuscript should emphasize principles as
   much as possible, rather than the GitHub realization of those
   principles; I realize that GitHub does a great job of bringing
   bioinformatics developers into the modern age. Minimally, I think
   that Git and GitHub should be removed from the title and all
   'Rules' headers.

4. The merits of individual recommendations should be reinforced with
   links to relevant examples, e.g., of an open issue, relevant
   commentary, and appropriate resolution. Similarly oriented links
   would help to convey the value / ease of continuous integration,
   and of test coverage.

5. The target audience is the relatively 'novice' developer; more
   established researchers will have their own procedures in place,
   will be aware of the current state-of-the-art, or will be too stuck
   in their ways to benefit from the discussion. From this
   perspective, it seems counter-productive to include 'organizations'
   and even 'teams' in rule 1; really one wants to get the individual
   or at most the individual + lab group oriented; 'organizations'
   (including the GitHub concept) are not immediately relevant.

6. Rule 3 should be refined to emphasize that branches are really
   short-term departures from master; it is too easy for academic
   developers to lose track of the thrust of their project, or for
   individuals to work in isolation for extended periods, so that
   their contribution cannot easily be merged back to master.

7. Rule 5 should be clarified. It includes really two points. The
   first is the use of unit tests to ensure that the software is doing
   as advertised. The second is the practice of committing (to master)
   running code. Maybe it would be better to break these out, and go
   for the novelty of 11, rather than the familiar 10, rules.

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

9. Rule 9 does not mention the obvious, effective, and esssential
   method for promoting one's project -- publishing in the
   peer-reviewed scientific literature!

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

2. Pg. 1, Introduction, para1: "Here, we introduce the main features
   of GitHub, a popular web-based 14 platform which offers a free and
   integrated environment for hosting the source code, documentation
   and web page for open source projects."

   Probably a better way to word ‘web page’, something like ‘public
   project-related web content’ since many projects are more complex.

3. Pg. 2, Introduction, para 2: small revision suggestion 

   “These rules have been ordered to reflect a typical development
   process: learning git and GitHub basics, use of branches, labeling
   and tagging of code snapshots, tracking project bugs and
   enhancements using issues, etc”

4. Pg. 2, Rule 1:

    a) Might be worth explaining what 'forking' means.

    b) "Structuring your projects allows to manage permissions and restrict
    access at different levels: users, teams and organisations."  Maybe "Project
    managers can structure projects to manage…"

    c) Repositories: The bit on repositories should be described earlier, not at
    the end.  You are technically forking a *repository*, not just a project
    (which in my opinion could consist of many independent but related
    repositories, e.g. the Bio* projects, GMOD, etc).

5. Pg. 3, Rule 2:

    a) "The cornerstone of GitHub is the distributed version control system git.
    Every change, from fixing a typo to a complete redesign of the software, is
    controlled by versions, so-called revisions." (added a comma after
    'software')

6. Pg. 3, Rule 3:

    a) "Nevertheless, one can always pull the currently up-to date master branch
    into one branch, enabling one to react or adapt to the changes in the stable
    code branch." (use 'branch', not 'fork')

    b) "Once a pull request is opened for review and discussion, it usually
    results in additional insights and increased code quality" ('it' was
    ambiguous)

7. Pg. 5, Rule 8:

    a) "The main motivation behind this is to give scientists a better credit
    for their work".  True, but this is also key for grants and funding, where
    many funding agencies such as NIH now accept other 'products' of research as
    citable research (these being publicly accessible data and software).

    b) https://guides.github.com/activities/citable-code/
    Should be consistent w/ other URLs in text

    c) ‘On one hand… on the other hand’ usually are used to describe two sides
    or opposing viewpoints. Not sure it’s used correctly here, since both
    examples are complementary, not in opposition to one another?

Chris Fields
