

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
 





 
 