Assignments in this directory ask you to solve problems in [`QuARK/notebooks`](https://github.com/econ-ark/QuARK):
   * https://github.com/econ-ark/QuARK contains 'Questions using the ARK'

To prepare for these assignments:

## Make A Fork of the QuARK Repo

1. Log into your GitHub account and navigate to [https://github.com/econ-ark/QuARK](https://github.com/econ-ark/QuARK)
1. Make a fork of the QuARK repo
   * Click the "Fork" button on the right of the `QuARK` repo
1. Clone your fork to your local `GitHub` directory; on unix, maybe `~/GitHub`
   * `cd ~/GitHub/[your-GitHub-ID]`
   * `git clone https://github.com/[your-GitHub-ID]/QuARK`
1. If you already have a fork of the `QuARK`, update it
   * The term for the original repo, is the "upstream" repo
   * 'update' your fork from the upstream repo (`QuARK`)
   * Google should tell you the commands you need to use. e.g., search
      * `how do I update my fork of a repo with changes to the upstream source repo`
   * Please __do NOT__ make a new fork without first deleting your original fork
      * GitHub keeps track of all the forks
	    * It becomes hopelessly confusing if one person has several forks


## For Each Assignment:

#### 0. Update Your `QuARK` fork (see above)
#### 1. Checkout A Branch Containing Your Name

1. In `QuARK/notebooks` you will find `[assignment-name].ipynb`
   * For example, `LifeCycleModelTheoryVsData-Problems.ipynb`
   1. Make a branch called `[assignment-name-your-github-username]`
	  * If I were a student, from the directory at the root of my cloned fork:
	     * `git checkout -b LifeCycleModelTheoryVsData-ccarrollATjhuecon`
   1. In the branch, make a copy, add `-And-Solutions` and make it writeable:
      * `cp [assignment-name].ipynb [assignment-name]-And-Solutions.ipynb`
	  * e.g.: `cp LifeCycleModelTheoryVsData-Problems.ipynb LifeCycleModelTheoryVsData-Problems-And-Solutions.ipynb`
      * `chmod u+w [assignment-name]-And-Solutions.ipynb`
   1. Open your `[assignment-name]-And-Solutions` notebook
      * `jupyter lab` from the command line in the notebooks directory

#### 2. Add `# SOLUTION` cell(s)
   1.  Read through the notebook
       * After each cell containing `# PROBLEM` produce a cell named `# SOLUTION`
       * If your solution uses more than one cell, label each with `# SOLUTION`

#### 3. Make A Pull Request With Your Solution
1. `commit` your changes to your branch
1. `push` your local branch to the your `remote` fork at your ID on `GitHub.com`
1. From your GitHub account, make a `pull request` to the upstream master
