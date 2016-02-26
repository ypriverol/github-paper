

## Section 1: Git LSF file system

Git Large File Storage (LFS) replaces large files (> 50 Mb)such as audio samples, videos, datasets, and graphics with text pointers inside Git, while
storing the file contents. In order to use the git _lfs_ service for big files, the user can follows the next steps: 


 1- Download the git plugin from here https://git-lfs.github.com/ or using Homebrew
 
```bash

   brew install git-lfs

```
  
 2- Select the file types you'd like Git LFS to manage (or directly edit your .gitattributes). You can configure additional file extensions at anytime.

```bash
 
   git lfs track "*.psd"

```   

3 -There is no step three. Just commit and push to GitHub as you normally would.

```bash
 
  git add file.psd
  
  git commit -m "Add design file"
  
  git push origin master
 
``` 


One of the major concerns about the use of GitHub is that some of the services are limited and can be charged if the users exceed certain quotes. For example, the Git LSF filesystem is available for all type of projects: personal repositories or organization accounts. A minimal space is provided for personal/organization repositories without charge
(1GB). If you exceed this quota, you can still clone repositories with large assets, but you will only retrieve the pointer files, and you will not be able to push new files back up.
 

## Section 2: Testing Levels and Continues integration

Software testing refers to the practice of testing certain functions and areas of our software code. It can be slitted in different categories or levels of complexity from unit tests to system testing. We would explain 
in details Unit tests and integration tests which are the start point to provide a functional software to the community. 

Unit testing is piece of code in your project which test individual units of source code, sets of one or more modules together with associated control data, usage procedures, and operating procedures. Ultimately, this helps us to identify failures in 
our algorithms and/or logic to help improve the quality of the code. These types of tests are usually written by developers as they work on code (white-box style), to ensure that the specific function is working 
as expected. One function might have multiple tests, to catch corner cases or other branches in the code. Unit testing alone cannot verify the functionality of a piece of software, but rather is used to ensure that the building
blocks of the software work independently from each other. 


```java
public class TestPTM {

    // can it add the positive numbers 1 and 1?
    public void testPTMIdentifier() {
        PTM ptm = new PSIModPTM();
        assert(ptm.parent.add(1, 1) == 2);
    }
}
```

Unit testing finds problems early in the development cycle. This includes both bugs in the programmer's implementation and flaws or missing parts of the specification for the unit.
The process of writing a thorough set of tests forces the author to think through inputs, outputs, and error conditions, and thus more crisply define the unit's desired behavior.
Some argue that code that is impossible or difficult to test is poorly written, thus unit testing can force developers to structure functions and objects in better ways. The unit tests can 
be more complex to explore the _logic_ of your code by testing the exptected results of an specific algorithm or mnathematical model. 


```java 

@Test
public void TestGetPTms() {
     List<PTM> ptms = modReader.getPTMListByPatternDescription("Phospho");
     assertTrue("Number of PTMs with Term 'Phospho' in name:", ptms.size() == 106);
}

```

However, when your software is run, all those units and modules have to work together, and the whole is more complex and subtle than the sum of its independently-tested parts. 
Proving that components _X_ and _Y_ both work independently doesn’t prove that they’re compatible with one another or configured correctly. Problems during this interaction  
may bear no relationship to the symptoms an end user would experience and report. If you automate this sort of 'component interaction' testing in order to detect breakages when they happen in the future, 
it’s called integration testing and typically uses different techniques and technologies than unit testing.  

Integration testing is the phase in software testing in which individual software modules are combined and tested as a group. It occurs after unit testing and before validation testing. 
Integration testing takes as its input modules that have been unit tested, groups them in larger aggregates, applies tests defined in an integration test plan to those aggregates, and delivers as its output 
the integrated system ready for system testing. 

With Travis-CI () the user can test their software and the following dependencies, see the following example from pIR package (https://github.com/ypriverol/pIR/):


```bash

sudo: required
language: c

before_install:
  - curl -OL http://raw.github.com/craigcitro/r-travis/master/scripts/travis-tool.sh
  - chmod 755 ./travis-tool.sh
  - ./travis-tool.sh bootstrap

install:
  - ./travis-tool.sh install_bioc BiocInstaller
  - ./travis-tool.sh install_deps
  - ./travis-tool.sh r_install knitr

script: ./travis-tool.sh run_tests

on_failure:
  - ./travis-tool.sh dump_logs

notifications:
  email:
    on_success: ypriverol@gmail.com 
    on_failure: ypriverol@gmail.com

after_failure:
  - ./travis-tool.sh dump_logs


```

The provided example installed all the dependencies of the library (BiocInstaller) and run all the corresponding tests in the R package. More documentation about
the Travis-CI integration can be found here https://travis-ci.org/ . 




 
 