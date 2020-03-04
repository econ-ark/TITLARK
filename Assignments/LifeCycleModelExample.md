
This assignment asks you to solve some problems posed in a notebook in the "QuARK" repo ("Questions made using the ARK")

Your assignment is:

1. Log into your GitHub account, navigate to https://github.com/econ-ark/QuARK, and make a fork of the QuARK repo
1. Clone your fork to your local machine:
   * `cd ~/GitHub/[your-GitHub-ID] ; git clone https://github.com/[your-GitHub-ID]/QuARK`
1. (If you already had a local clone of a fork of the QuARK repo, perhaps in `~/GitHub/econ-ark-forks` you might want to update it (though you should use the clone of your own fork for the assignment; updating in `econ-ark-forks` is purely so that you can have the original version as a reference)
   * Google should tell you the commands you need to use
   * The term for the original repo, is the "upstream" repo
   * If you can't figure out how to do this, you can
      1. Delete the original fork from last week
	  1. Make a new fork
   * Please do NOT make a new fork without first deleting your original fork
      * GitHub keeps track of all the forks
	  * It becomes hopelessly confusing if one person has several forks
1. In QuARK/notebooks you will find `LifeCycleModelExample-Problems.ipynb`
   1. Make a branch called '[your-github-username]'
	  * if I were a student: `git checkout -b ccarrollATjhuecon`
   1. In the branch, make a copy and make it writeable:
      * `cp LifeCycleModelExample-Problems.ipynb LifeCycleModelExample-Problems-And-Solutions.ipynb`
	  * `chmod u+w LifeCycleModelExample-Problems-And-Solutions.ipynb`
   1. Open the notebook
      * `jupyter notebook` from the command line in the notebooks directory
   1.  Read through this notebook, and solve the multi-part problem '"Luck" and Saving' at the end
1. When you have finished solving the problem:
   1. "push" your local copy to the your "remote" version of the fork on at your ID on GitHub.com
   1. From your GitHub.com account, issue a "pull request" to the upstream master

PS. The second problem, "Saving Rates and Wealth Levels", is harder, and optional
