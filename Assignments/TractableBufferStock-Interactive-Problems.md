# What Happens As the GIF Approaches Its Limit?

(If you do not yet have a fork of TITLARK on your virtual machine, you might want to read the [instructions here](https://github.com/econ-ark/HARK/blob/master/doc/guides/contributing/issues.md#linking-your-fork-to-your-local-clone) which cover a slightly different case -- for making contributions to the HARK repo -- but it should be easy to translate to TITLARK)

Your assignment is:

1. Update your local fork of the TITLARK repo 
   * Google should tell you the commands you need to use
   * The term for the original repo, is the "upstream" repo
   * If you can't figure out how to do this, you can
      1. Delete the original fork from last week
	  1. Make a new fork
   * Please do NOT make a new fork without first deleting your original
      * GitHub keeps track of all the forks
	  * It becomes hopelessly confusing if one person has several forks
1. In TITLARK/notebooks you will find `TractableBufferStock-Interactive-Problems.ipynb`
   1. Make a branch called '[your-github-username]TractableSolution'
	  * if I were a student: `git checkout -b ccarrollATjhueconTractableSolution`
   1. In the branch, make a copy:
      * `cp TractableBufferStock-Interactive-Problems.ipynb TractableBufferStock-Interactive-Solutions.ipynb`
   1. Open the notebook
      * `jupyter notebook` from the command line in the notebooks directory
   1.  Read through this notebook, and solve the problem at the end
1. When you have finished solving the problem:
   1. "push" your local copy to the your "remote" version of the fork on GitHub.com
   1. From your GitHub.com account, issue a "pull request" to the upstream master
