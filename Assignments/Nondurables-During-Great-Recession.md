# Nondurables-During-Great-Recession

This assignment asks you to solve some problems posed in a notebook in the "QuARK" repo ("Questions made using the ARK")

Your assignment is:

## Make A Fork of the QuARK Repo 

You can skip the instructions below if you already have a fork of the QuARK

1. On [GitHub.com](https://github.com), Log into your GitHub account from a browser (FireFox is the VM's default)
1. Navigate to https://github.com/econ-ark/QuARK, and make a fork of the QuARK repo
   * Click the "Fork" button on the right
1. Clone your fork to your local machine:
   * `cd ~/GitHub/[your-GitHub-ID] ; git clone https://github.com/[your-GitHub-ID]/QuARK`
1. (If you already had a local clone of a fork of the QuARK repo, perhaps in `~/GitHub/econ-ark-forks` you should update it (though you should use the clone of your own fork for the assignment; updating in `econ-ark-forks` is purely so that you can have the original version as a reference)
   * Google should tell you the commands you need to use: Search "how do I update my fork of a repo with changes to the upstream source repo"
   * The term for the original repo, is the "upstream" repo
   * If you can't figure out how to do this, you can
      1. Delete the original fork 
		 * Both on GitHub.com and on our local machine
	  1. Make a new fork
   * Do NOT make a new fork without first deleting your original fork
      * GitHub.com keeps track of all the forks
	  * It becomes hopelessly confusing if one person has several forks

## Checkout A Branch Containing Your Name

In your local copy of your fork of the QuARK, you will find in the notebooks directory `Nondurables-During-Great-Recession-Problems.ipynb`
	  * `cd ~/GitHub/[your-GitHub-ID]/QuARK/notebooks`
   1. Make a branch called '[your-github-username]Solutions'
	  * if I were a student: `git checkout -b ccarrollATjhueconSolutions`
	  * if it already exists: `git checkout ccarrollATjhueconSolutions`

## Copy the notebook and make it writeable:
   1. Make your solutions notebook
   * `cp Nondurables-During-Great-Recession-Problems.ipynb Nondurables-During-Great-Recession-Problems-And-Solutions.ipynb`
   * `chmod u+w Nondurables-During-Great-Recession-Problems-And-Solutions.ipynb`
   1. Open the notebook
      * `jupyter lab` from the command line in the notebooks directory
   1.  Read through the notebook, and create (or fill in) "SOLUTION" cells after the "PROBLEM" cells

## Turn In the Assignment
   1. "push" your local copy to the your "remote" version of your fork at your ID on GitHub.com
   1. In your browser, return to your GitHub.com account, issue a "pull request" to the upstream QuARK repo
   1. Go to `https://github.com/econ-ark/QuARK` and verify that there is a PR from your fork
