(Warning: Internal links -- say, to references -- [do not work](https://tex.stackexchange.com/questions/264227/pandoc-breaks-hyperlinks-in-latex-file-conversion) here)

(They _do_ work in [the html version](https://econ-ark.github.io/TITLARK/Courses/HA-Macro/2020-04-Oz/syllabus/syllabus-Oz.html))

Hands-On Heterogeneous Agent Macroeconomics Using the
[Econ-ARK/HARK](http://econ-ark.org) Toolkit

[Christopher D. Carroll](http://www.econ2.jhu.edu/people/ccarroll)

Syllabus for Hands-On Heterogeneous Agent Macroeconomics

Australian National University℘ 

April, 2020

Because Representative Agent (‘RA’) models were not useful for
understanding much of what happened in the Great Recession, policymakers
including Larry [Summers](#XsummersWolf2) ([2011](#XsummersWolf2)), Fed
Chair Janet [Yellen](#XyellenHetero) ([2016](#XyellenHetero)), former
IMF Chief Economist Olivier
[Blanchard](#XblanchardDSGE) ([2016](#XblanchardDSGE)), ECB Governing
Board Member Benoit [Coeure](#XcoeureHetero) ([2013](#XcoeureHetero)),
and Bank of England Chief Economist
Andy [Haldane](#XhaldaneDappled) ([2016](#XhaldaneDappled)) have
suggested that incorporation of heterogeneity (for example, across
borrowers and lenders) must be an essential part of the agenda in
developing new and better models. In confirmation of that intuition, a
number of recent papers, most notably [Kaplan, Moll, and
Violante](#XkmvHANK) ([2018](#XkmvHANK)) and [Krueger, Mitman, and
Perri](#XkmpHandbook) ([2016](#XkmpHandbook)), have developed models
that include a realistic description of microeconomic heterogeneity, and
have shown that such models can generate more sensible macroeconomic
implications than RA models for important questions like the operation
of fiscal and monetary policy.

This course will provide a hands-on introduction to the construction of
models with ‘serious’ heterogeneity (that is, heterogeneity that matches
the microeconomic facts that theory suggests should matter for
macroeconomic outcomes like consumption dynamics); why such
heterogeneous agent (‘HA’) models have implications different from those
of RA models; and how existing HA models can be adapted to new
questions. (‘Hands-On’ means that students with their own laptops will
run the and experiment with the code that solves these models in class.)

The course will have two main elements: Lectures explaining the
conceptual foundations of the models work; and hands-on demonstrations
of live working versions of such models using the open-source
[Econ-ARK/HARK](http://econ-ark.org/HARK) toolkit.

Students should bring a laptop on which they have permissions to install
and run new software. Prior to class, on that laptop, students should
have installed the
[anaconda3](https://www.anaconda.com/what-is-anaconda/) stack, which is
a distribution of python 3 that includes a robust set of extra tools
that are useful for doing computational work. A good guide to installing
anaconda is
[here](https://github.com/mmcky/nyu-econ-370/blob/master/install-local-guide.pdf).

(In “readings” below, starred readings are strongly suggested)

### 1  Preliminaries

Certain things must be done to prepare for running everything on your
own computer

#### 1.1  Option 1: Do Everything On Your Own Computer’s OS

1.  Install [Anaconda](https://docs.anaconda.com/anaconda/install):
    [https://docs.anaconda.com/anaconda/install](https://docs.anaconda.com/anaconda/install)
2.  Get Git
    -   [Get the command-line
        tool](https://atlassian.com/git/tutorials/install-git):
        -   [https://atlassian.com/git/tutorials/install-git](https://atlassian.com/git/tutorials/install-git)
    -   [Get a GitHub Account](https://github.com/join)
    -   [Download the GitHub Desktop App](https://desktop.github.com)
        -   And connect it to your online GitHub account
3.  [Install HARK](https://github.com/econ-ark/HARK#content-install)
    -   Follow the instructions for installing HARK for Anaconda
4.  Clone the [DemARK](https://github.com/econ-ark/DemARK) and
    [REMARK](https://github.com/econ-ark/REMARK) repos
    -   git clone https://github.com/econ-ark/DemARK
    -   git clone https://github.com/econ-ark/REMARK
5.  Using python from the command line:
    -   pip install nose
    -   python -c ’import HARK ; print(HARK.\_\_file\_\_)’
    -   cd \[root directory for HARK\]
    -   python -m nose

#### 1.2  Option 2: Do Everything On a Virtual Machine

1.  Find (or buy) free space of at least 100 GB
    -   A FAST flash/pen drive is fine (not a slow one)
2.  Follow the instructions [for installing your
    VM](https://github.com/econ-ark/econ-ark-tools/tree/master/Virtual/Machine/VirtualBox)

### 2  Motivation

Models with serious microfoundations yield fundamentally different
conclusions than RA models about core questions in macroeconomics.

1.  How monetary policy works
    -   HA channels account for most of the mechanism of monetary
        transmission
2.  Whether fiscal policy works
    -   ‘serious’ HA models are consistent with evidence of MPC’s of 0.5
3.  What made the Great Recession Great
    -   RA models: Mostly a supply shock
    -   HA models: Mostly a demand shock

Slides:

-   [Intro to Monetary Policy with
    Heterogeneity](https://github.com/llorracc/resources/blob/master/Slides/CrawleyMonPolicywithHeterogeniety.pdf),
    [Crawley](#XCrawleyMonPolicywithHeterogeneity) ([2019](#XCrawleyMonPolicywithHeterogeneity))

Readings:

-   [](http://www.princeton.edu/~moll/WIMM.pdf)[Ahn, Kaplan, Moll,
    Winberry, and Wolf](#XakmwwInequality) ([2017](#XakmwwInequality)),
    Introduction, Conclusion
    -   Compact and well written discussion of the state and progress of
        HA macro.
-   [Carroll and
    Crawley](#XakmwwInequality-Discuss) ([2017](#XakmwwInequality-Discuss)),
    [Sections 1, 2, and
    4](http://econ.jhu.edu/people/ccarroll/discuss/2017-04_NBER_Macro-Annual/akmwwInequality/)
    -   This discussion of that paper puts the relationship of HA to RA
        models in context.

### 3  The Relation Between Micro and Macro Models

#### 3.1  The Relation Between Micro and Macro Models

It has become clear in the last decade (and especially in the last few
years) that the micro and macro parts of the HA macro problem are
surprisingly independent. HA macro models can be solved by first using
powerful tools to find the steady state of the micro problem, and then
using other tools to calculate how the micro solution changes over the
business cycle. Relatively small – or even linear – changes to even a
highly nonlinear microeconomic problem can result in quantitatively
plausible macroeconomic dynamics. p Readings:

-   [Reiter](#XreiterSolving) ([2009](#XreiterSolving))
-   [Boppart, Krusell, and
    Mitman](#XbmpMITshocks) ([2018](#XbmpMITshocks))
-   [Auclert](#XauclertMonetary) ([2019](#XauclertMonetary))
-   [Heterogeneity and Macro Modeling In Policymaking
    Institutions](https://mybinder.org/v2/gh/econ-ark/PARK/master?filepath=Hetero-And-Macro/Hetero-And-Macro.ipynb),

### 4  Micro Models

#### 4.1  Micro Consumption Theory Refresher

The course will assume that students are familiar with standard
quantitative tools for solving RA models, like DYNARE. The bulk of the
“hands-on” part of the course will therefore involve learning and using
tools for solving micro problems with ‘serious’ microfoundations.

##### 4.1.1  The Infinite Horizon Perfect Foresight Model

Kinds of Impatience: Absolute, Return, and Growth

Notes:

-   [Consumption Under Perfect Foresight and CRRA
    Utility](http://econ.jhu.edu/people/ccarroll/public/LectureNotes/Consumption/PerfForesightCRRA/)
-   [The Certainty Equivalent Consumption
    Function](http://econ.jhu.edu/people/ccarroll/public/LectureNotes/Consumption/ConsumptionFunction/)

##### 4.1.2  Consumption With Labor Income Uncertainty

-   Notes:    [A Tractable Model of Buffer Stock
    Saving](http://econ.jhu.edu/people/ccarroll/public/LectureNotes/Consumption/TractableBufferStock/)
-   Notebook: [Interactive
    Demo](https://econ-ark.org/materials/TractableBufferStock-Interactive)

##### 4.1.3  Rate-Of-Return Uncertainty without Labor Income

Under CRRA utility, without labor income risk:

1.  The consumption function is linear
2.  An increase in risk reduces consumption and the MPC

Notes:

-   [Consumption out of Risky
    Assets](http://econ.jhu.edu/people/ccarroll/public/LectureNotes/Consumption/CRRA-RateRisk/)
    -   (Unavoidably) Riskier Returns ![⇒ ](syllabus-Oz6x.svg) lower ![C
        ](syllabus-Oz7x.svg) (if ![ρ \> 1 ](syllabus-Oz8x.svg))
-   [Portfolio Choice with CRRA
    Utility](http://econ.jhu.edu/people/ccarroll/public/LectureNotes/AssetPricing/CRRA-Portfolio/)
    -   Greater financial risk ![⇒ ](syllabus-Oz9x.svg) Smaller
        Portfolio Share (![ς ↓ ](syllabus-Oz10x.svg))
-   [Consumption With Portfolio
    Choice](http://econ.jhu.edu/people/ccarroll/public/LectureNotes/AssetPricing/C-With-Optimal-Portfolio/):
    ![σr ↑ ⇒ ↑ ](syllabus-Oz11x.svg) in ![C ](syllabus-Oz12x.svg) (!)
    -   You reduce your exposure to risk
    -   Total eventual portfolio risk is less than before ![σr ↑
        ](syllabus-Oz13x.svg)
    -   Precautionary saving ![↓ ](syllabus-Oz14x.svg)
    -   Net result: ![σr ↑⇒ C ↑ ](syllabus-Oz15x.svg)
-   [ConsPortfolioModel](https://econ-ark.org/materials/ConsPortfolioModelDoc)
    -   “Stockholding Puzzle” [Bertaut and
        Haliassos](#Xbertaut&haliassos:portfolio) ([1997](#Xbertaut&haliassos:portfolio))

Origins: [Merton](#Xmerton:restat) ([1969](#Xmerton:restat)),
[Samuelson](#Xsamuelson:portfolio) ([1969](#Xsamuelson:portfolio))

##### 4.1.4  Habits

Notes:

-   [Consumption Models with Habit
    Formation](http://econ.jhu.edu/people/ccarroll/public/LectureNotes/Consumption/Habits/):
    -   ![Δ logct+1 = (1 − α)þr + αΔ log ct ](syllabus-Oz16x.svg)

### 5  Computational Tools

#### 5.1  Vision for the Econ-ARK Project

-   [Intro-To-Econ-ARK](https://github.com/econ-ark/PARK/blob/master/Intro-To-Econ-ARK-Overlay.pdf)

#### 5.2  Intro to Heterogeneous Agents Resources and Toolkit (HARK)

-   [Intro-To-HARK](https://github.com/econ-ark/PARK/blob/master/Intro-To-HARK-Overlay.pdf)

### 6  Hands-On Introduction

Here we will explain how to begin using the
[Econ-ARK](http://econ-ark.org) toolkit for heterogeneous agent macro
modeling. Students will be taught how to use the toolkit to solve
increasingly sophisticated models, starting with partial equilibrium
perfect foresight models and ending with some exercises using a full
general equilibrium micro-macro model with idiosyncratic and aggregate
risks.

#### 6.1  A Gentle Introduction

This section builds our first simple models using the toolkit

##### 6.1.1  Perfect Foresight

Notebook: [A Gentle Introduction to HARK - Perfect
Foresight](https://econ-ark.org/materials/gentle-intro-to-hark-perfforesightcrra)

##### 6.1.2  Adding ‘Serious’ Income Uncertainty

Notebook: [A Gentle Introduction to Buffer Stock
Saving](https://econ-ark.org/materials/Gentle-Intro-To-HARK-Buffer-Stock-Model)

#### 6.2  Liquidity Constraints, Precautionary Saving, and Impatience

1.  The Growth Impatience Condition
2.  Liquidity Constraints and Precautionary Saving
3.  Impatience and Target Wealth

Notebook: [BufferStockTheory
Problems](https://econ-ark.org/materials/BufferStockTheory-Problems.ipynb)

#### 6.3  ‘Serious’ Wealth Inequality

Notebook:
[Micro-and-Macro-Implications-of-Very-Impatient-HHs](https://econ-ark.org/materials/micro-and-macro-implications-of-very-impatient-hhs)

References: [Carroll, Slacalek, Tokuoka, and
White](#XcstwMPC) ([2017](#XcstwMPC))

#### 6.4  Matching the Distribution – of the MPC

-   : [Figure
    5,](http://www.econ2.jhu.edu/people/ccarroll/papers/cstwMPC/#x1-130075)
    [Carroll, Slacalek, Tokuoka, and
    White](#XcstwMPC) ([2017](#XcstwMPC))
-   : [Figure
    10b,](https://github.com/llorracc/Figures/blob/master/Crawley-MPC-By-Liquid-Assets.png)
    [Crawley and Kuchler](#XckConsumption) ([2018](#XckConsumption))

#### 6.5  Hands-On with Real HA Models

For an economy in steady state (that is, with constant factor prices
like interest rates and wages), models with ‘serious’ income
heterogeneity have been solvable in partial equilibrium since about 1990
([Zeldes](#XzeldesStochastic) ([1989](#XzeldesStochastic)),
[Deaton](#XdeatonLiqConstr) ([1991](#XdeatonLiqConstr))). Calculating an
equilibrium distribution of wealth that results from those policy
functions and matching it to the total amount of observed wealth (and a
corresponding interest rate) was first done by [Hubbard, Skinner, and
Zeldes](#Xhsz:importance) ([1994](#Xhsz:importance)) using a
supercomputer. [Aiyagari](#Xaiyagari:ge) ([1994](#Xaiyagari:ge))
proposed a radically simple model that did not attempt to match the
distributions of wealth and income, but could be solved without a
supercomputer.

In a rational expectations steady state, there are no expected changes
in interest rates, wages, or the distribution. Aggregate fluctuations
make calculation of an RE equilibrium massively more difficult, because:

1.  Meaningful aggregate fluctuations will change the distribution of
    wealth and income
2.  The amount of aggregate saving depends on how aggregate wealth and
    income are distributed
3.  The amount of saving determines future factor prices
4.  In principle, RE therefore requires that everyone know the entire
    distribution of wealth, income, and any other state variables in the
    population

The problem therefore suffers from a severe case of the “curse of
dimensionality.” (That is, it’s really hard!). The first paper to tackle
the problem was [Krusell and Smith](#XksHetero) ([1998](#XksHetero)).
Work by [Bayer and Luetticke](#XblSolving) ([2018](#XblSolving)) builds
on all of the prior work to construct a reasonable HANK model that can
be solved in a few minutes on a laptop. The key contribution of [Krusell
and Smith](#XksHetero) ([1998](#XksHetero)) was to discover that, in
practice, highly accurate predictions of future aggregate states could
be made using only the mean of the current aggregate capital stock

Notebook:
[KrusellSmith.ipynb](https://econ-ark.org/materials/KrusellSmith.ipynb)

#### 6.6  The Micro Steady State and Macro Fluctuations

A problem with solving methods using the original Krusell Smith method
is that the computational challenge was so great that only the simplest
such models could be solved, and the ability to construct standard tools
like impulse response functions to aggregate shocks was very limited.

[Reiter](#XreiterSolving) ([2009](#XreiterSolving)) showed how to solve
such problems several orders of magnitude faster; the essence of his
idea was to solve the micro problem for the steady-state distribution,
and then capture business cycle fluctuations by figuring out how to
perturb the decision rules and the distribution appropriately.

Building on his work, the last few years have seen great further strides
in speed and power of such tools.

References:

-   [Reiter](#XreiterSolving) ([2009](#XreiterSolving))
-   [Boppart, Krusell, and
    Mitman](#XbmpMITshocks) ([2018](#XbmpMITshocks))
-   [Ahn, Kaplan, Moll, Winberry, and
    Wolf](#XakmwwInequality) ([2017](#XakmwwInequality))
-   [Bayer and Luetticke](#XblSolving) ([2018](#XblSolving))

#### 6.7  The Bayer-Luetticke Method

-   Notebooks:
    -   [OneAsset HANK
        Model](https://mybinder.org/v2/gh/econ-ark/HARK/master?filepath=HARK/BayerLuetticke/notebooks/OneAsset-HANK.ipynb)
    -   [TwoAsset HANK
        Model](https://mybinder.org/v2/gh/econ-ark/HARK/master?filepath=HARK/BayerLuetticke/notebooks/TwoAsset.ipynb)
    -   [DCT-Copula-Illustration](https://mybinder.org/v2/gh/econ-ark/HARK/master?filepath=HARK/BayerLuetticke/notebooks/DCT-Copula-Illustration.ipynb)

#### 6.8  Other Literature

References:

-   [Monetary Policy Transmission with Many
    Agents](https://github.com/llorracc/Resources/blob/master/Papers/SSinHANK.pdf),
    [Crawley and Lee](#XSSinHANK) ([2019](#XSSinHANK))
-   [Macroprudential Policies in a Heterogeneous Agent Model of Housing
    Default](https://pdfs.semanticscholar.org/8e9d/dfe7c204bbfa8a23f42f4931461fb467fc08.pdf?_ga=2.95712860.1156899890.1563925023-1991616136.1563925023),
    [Khan](#XkhanMacroPru) ([2019](#XkhanMacroPru))
-   [Redistribution, risk premia, and the
    macroeconomy](https://github.com/llorracc/resources/blob/master/Slides/klRiskPremia.pdf),
    [Kekre and Lenel](#XklRiskPremia) ([2019](#XklRiskPremia))
-   [The Missing Intercept: A Sufficient Statistics Approach to General
    Equilibrium
    Effects](https://github.com/llorracc/resources/blob/master/Slides/wolfGE-invariance.pdf),
    [Wolf](#XwolfGEInvariance) ([2019](#XwolfGEInvariance))

### 7  Take Home Exam

The exam in this class will be a take-home exam in which the students
will be expected to use the modeling techniques they have learned to
make a meaningful substantive extension of one of the models they have
learned in class. Their code will be tested to determine whether it
works, and then judged on the basis of how well the extension has been
done.

### References

   Ahn, SeHyoun, Greg Kaplan, Benjamin Moll, Thomas Winberry, and
Christian Wolf (2017): “When Inequality Matters for Macro and Macro
Matters for Inequality,” NBER Macroeconomics Annual, 32.

   Aiyagari, S. Rao (1994): “Uninsured Idiosyncratic Risk and Aggregate
Saving,” Quarterly Journal of Economics, 109, 659–684.

   Auclert, Adrien (2019): “Monetary policy and the redistribution
channel,” American Economic Review, 109(6), 2333–67,
<https://pubs.aeaweb.org/doi/pdfplus/10.1257/aer.20160137>.

   Bayer, Christian, and Ralph Luetticke (2018): “Solving Heterogeneous
Agent Models In Discrete Time With Many Idiosyncratic States By
Perturbation Methods,” Centre for Economic Policy Research, Discussion
Paper 13071.

   Bertaut, Carol C., and Michael Haliassos (1997): “Precautionary
portfolio behavior from a life-cycle perspective,” Journal of Economic
Dynamics And Control, 21(8-9), 1511–1542.

   Blanchard, Olivier (2016): “Do DSGE Models Have a Future?,”
Discussion paper, Petersen Institute for International Economics,
Available at <https://piie.com/system/files/documents/pb16-11.pdf>.

   Boppart, Timo, Per Krusell, and Kurt Mitman (2018): “Exploiting MIT
Shocks in Heterogeneous-Agent Economies: The Impulse Response as a
Numerical Derivative,” Journal of Economic Dynamics and Control, 89(C),
68–92.

   Carroll, Christopher D., and Edmund Crawley (2017): “Discussion of
‘When Inequality Matters for Macro and Macro Matters for Inequality’,”
Discussion paper, NBER.

   Carroll, Christopher D., Jiri Slacalek, Kiichi Tokuoka, and
Matthew N. White (2017): “The Distribution of Wealth and the Marginal
Propensity to Consume,” Quantitative Economics, 8, 977–1020, At
[http://econ.jhu.edu/people/ccarroll/papers/cstwMPC](http://econ.jhu.edu/people/ccarroll/papers/cstwMPC).

   Coeure, Benoit (2013): “The relevance of household-level data for
monetary policy and financial stability analysis,” .

   Crawley, Edmund (2019): “Intro to Monetary Policy with
Heterogeneity,” Slides Presented at JHU “Computational Methods in
Economics”.

   Crawley, Edmund, and Andreas Kuchler (2018): “Consumption
Heterogeneity: Micro Drivers and Macro Implications,” working paper 129,
Danmarks Nationalbank.

   Crawley, Edmund, and Seungcheol Lee (2019): “Monetary Policy
Transmission with Many Agents,” Manuscript, Johns Hopkins University.

   Deaton, Angus S. (1991): “Saving and Liquidity Constraints,”
Econometrica, 59, 1221–1248,
[http://www.jstor.org/stable/2938366](http://www.jstor.org/stable/2938366).

   Haldane, Andy (2016): “The Dappled World,” Discussion paper, Bank of
England, Available at
<http://www.bankofengland.co.uk/publications/Pages/speeches/2016/937.aspx>.

   Hubbard, R. Glenn, Jonathan S. Skinner, and Stephen P. Zeldes (1994):
“The Importance of Precautionary Motives for Explaining Individual and
Aggregate Saving,” in The Carnegie-Rochester Conference Series on Public
Policy, ed. by Allan H. Meltzer, and Charles I. Plosser, vol. 40, pp.
59–126.

   Kaplan, Greg, Benjamin Moll, and Giovanni L. Violante (2018):
“Monetary Policy According to HANK,” American Economic Review, 108(3),
697–743.

   Kekre, Rohan, and Moritz Lenel (2019): “Redistribution, risk premia,
and the macroeconomy,” Slides Presented at NBER ‘Micro to Macro’ Working
Group.

   Khan, Shujaat (2019): “Macroprudential Policies in a Heterogeneous
Agent Model of Housing Default,” Department of Economics, Johns Hopkins
University.

   Krueger, Dirk, Kurt Mitman, and Fabrizio Perri (2016):
“Macroeconomics and Household Heterogeneity,” Handbook of
Macroeconomics, 2, 843–921.

   Krusell, Per, and Anthony A. Smith (1998): “Income and Wealth
Heterogeneity in the Macroeconomy,” Journal of Political Economy,
106(5), 867–896.

   Merton, Robert C. (1969): “Lifetime Portfolio Selection under
Uncertainty: The Continuous Time Case,” Review of Economics and
Statistics, 51, 247–257.

   Reiter, Michael (2009): “Solving heterogeneous-agent models by
projection and perturbation,” Journal of Economic Dynamics and Control,
33(3), 649–665,
<https://www.sciencedirect.com/science/article/pii/S0165188908001528>.

   Samuelson, Paul A. (1969): “Lifetime Portfolio Selection by Dynamic
Stochastic Programming,” Review of Economics and Statistics, 51, 239–46.

   Summers, Lawrence H. (2011): “Larry Summers and Martin Wolf on New
Economic Thinking,” Financial Times interview,
[http://larrysummers.com/commentary/speeches/brenton-woods-speech/](http://larrysummers.com/commentary/speeches/brenton-woods-speech/).

   Wolf, Christian (2019): “The Missing Intercept: A Sufficient
Statistics Approach to General Equilibrium Effects,” Slides Presented at
NBER ‘Micro to Macro’ Working Group.

   Yellen, Janet (2016): “Macroeconomic Research After the Crisis,”
Available at
<https://www.federalreserve.gov/newsevents/speech/yellen20161014a.htm>.

   Zeldes, Stephen P. (1989): “Optimal Consumption with Stochastic
Income: Deviations from Certainty Equivalence,” Quarterly Journal of
Economics, 104(2), 275–298.
