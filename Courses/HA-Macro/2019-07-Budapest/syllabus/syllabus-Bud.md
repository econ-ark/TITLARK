### Hands-On Heterogeneous Agent Macroeconomics

Using the [Econ-ARK/HARK](http://econ-ark.org) Toolkit

February 9, 2019

[Christopher D. Carroll](http://www.econ2.jhu.edu/people/ccarroll)

Syllabus for a short course on Heterogeneous Agent Macroeconomics

Budapest School of Central Bank Studies

July, 2019

Because Representative Agent (‘RA’) models were not useful for understanding much of what happened in the Great Recession, policymakers including Larry [Summers](#XsummersWolf2) ([2011](#XsummersWolf2)), Fed Chair Janet [Yellen](#XyellenHetero) ([2016](#XyellenHetero)), former IMF Chief Economist Olivier [Blanchard](#XblanchardDSGE) ([2016](#XblanchardDSGE)), ECB Governing Board Member Benoit [Coeure](#XcoeureHetero) ([2013](#XcoeureHetero)), and Bank of England Chief Economist Andy [Haldane](#XhaldaneDappled) ([2016](#XhaldaneDappled)) have suggested that incorporation of heterogeneity (for example, across borrowers and lenders) must be an essential part of the agenda in developing new and better models. In confirmation of that intuition, a number of recent papers, most notably [Kaplan, Moll, and Violante](#XkmvHANK) ([2018](#XkmvHANK)) and [Krueger, Mitman, and Perri](#XkmpHandbook) ([2016](#XkmpHandbook)), have developed models that include a realistic description of microeconomic heterogeneity, and have shown that such models can generate more sensible macroeconomic implications than RA models for important questions like the operation of fiscal and monetary policy.

The aim of this course is to provide a hands-on introduction to the construction of models with ‘serious’ heterogeneity (that is, heterogeneity that matches the microeconomic facts that theory suggests should matter for macroeconomic outcomes like consumption dynamics); why such heterogeneous agent (‘HA’) models have implications different from those of RA models; and how existing HA models can be adapted to new questions. (‘Hands-On’ means that students with their own laptops will run the and experiment with the code that solves these models in class.)

The course will have two main components: Lectures explaining the conceptual foundations of the models work; and hands-on demonstrations of live working versions of such models using the open-source [Econ-ARK/HARK](http://econ-ark.org/HARK) toolkit.

Students should bring a laptop on which they have permissions to install and run new software. Prior to class, on a laptop that they should bring to class, students should have installed the [anaconda3](https://www.anaconda.com/what-is-anaconda/) stack, which is a distribution of python 3 that includes a robust set of extra tools that are useful for doing computational work. A good guide to installing anaconda is [here](https://github.com/mmcky/nyu-econ-370/blob/master/install-local-guide.pdf).

### 1  Motivation and Preliminaries

#### 1.1  Motivation

The introduction and conclusion to [Ahn, Kaplan, Moll, Winberry, and Wolf](#XakmwwInequality) ([2017](#XakmwwInequality))’s NBER Macro Annual paper provides a compact and well written discussion of the state and progress of HA macro.

[This discussion](http://econ.jhu.edu/people/ccarroll/discuss/2017-04_NBER_Macro-Annual/akmwwInequality/) of that paper puts the relationship of HA to RA models in context.

Notes:

-   [NBER-Macro-Annual-Heterogeneity-Discuss](https://www.econ2.jhu.edu/people/ccarroll/discuss/2017-04_NBER_Macro-Annual/akmwwInequality-Slides.pdf)

Readings:

-   [Ahn, Kaplan, Moll, Winberry, and Wolf](#XakmwwInequality) ([2017](#XakmwwInequality)), Introduction, Conclusion
-   [Carroll and Crawley](#XakmwwInequality-Discuss) ([2017](#XakmwwInequality-Discuss)), [Sections 1, 2, and 4](http://econ.jhu.edu/people/ccarroll/discuss/2017-04_NBER_Macro-Annual/akmwwInequality/)

#### 1.2  Micro Consumption Theory Refresher

##### 1.2.1  The Infinite Horizon Perfect Foresight Model

Notes:

-   [Consumption Under Perfect Foresight and CRRA Utility](http://www.econ2.jhu.edu/people/ccarroll/public/LectureNotes/Consumption/PerfForesightCRRA/)

##### 1.2.2  Consumption With Labor Income Uncertainty

-   Notebook: [Theoretical Foundations of Buffer Stock Saving](http://github.com/econ-ark/REMARK/tree/master/REMARKs/BufferStockTheory/BufferStockTheory-Problems.ipynb)

##### 1.2.3  The Special Case of Rate-Of-Return Uncertainty

Notes: [Consumption out of Risky Assets](http://www.econ2.jhu.edu/people/ccarroll/public/LectureNotes/Consumption/CRRA-RateRisk/)

Origins: [Merton](#Xmerton:restat) ([1969](#Xmerton:restat)), [Samuelson](#Xsamuelson:portfolio) ([1969](#Xsamuelson:portfolio))

### 2  Computational Tools

#### 2.1  Vision for the Econ-ARK Project

-   [Intro-To-Econ-ARK](https://github.com/econ-ark/PARK/blob/master/Intro-To-Econ-ARK-Overlay.pdf)

### 3  Hands-On Introduction

Here we will explain how to begin using the [Econ-ARK](http://econ-ark.org) toolkit for heterogeneous agent macro modeling, and will guide students through the use of the toolkit to solve increasingly sophisticated models, starting with partial equilibrium perfect foresight models and ending with some exercises using a full general equilibrium micro-macro model with idiosyncratic and aggregate risks.

#### 3.1  A Gentle Introduction

Notebook: [A Gentle Introduction to HARK](https://mybinder.org/v2/gh/econ-ark/DemARK/master?filepath=notebooks/Gentle-Intro-To-HARK.ipynb)

##### 3.1.1  Perfect Foresight

##### 3.1.2  Adding ‘Serious’ Income Uncertainty

###  References

    ahn, sehyoun, greg kaplan, benjamin moll, thomas winberry, and christian wolf (2017): “When Inequality Matters for Macro and Macro Matters for Inequality,” in NBER Macroeconomics Annual, ed. by Jonathan Parker, and Organizers Martin S. Eichenbaum, vol. 32, Cambridge, MA. MIT Press, Available at [http://www.princeton.edu/~moll/WIMM.pdf](http://www.princeton.edu/~moll/WIMM.pdf).

    blanchard, olivier (2016): “Do DSGE Models Have a Future?,” Discussion paper, Petersen Institute for International Economics, Available at <https://piie.com/system/files/documents/pb16-11.pdf>.

    carroll, christopher d., and edmund crawley (2017): “Discussion of ‘When Inequality Matters for Macro and Macro Matters for Inequality’,” in NBER Macroeconomics Annual. MIT Press, Available at [http://econ.jhu.edu/people/ccarroll/discuss/2017-04\_NBER\_Macro-Annual/akmwwInequality/](http://econ.jhu.edu/people/ccarroll/discuss/2017-04_NBER_Macro-Annual/akmwwInequality/).

    coeure, benoit (2013): “The relevance of household-level data for monetary policy and financial stability analysis,” .

    haldane, andy (2016): “The Dappled World,” Discussion paper, Bank of England, Available at <http://www.bankofengland.co.uk/publications/Pages/speeches/2016/937.aspx>.

    kaplan, greg, benjamin moll, and giovanni l. violante (2018): “Monetary Policy According to HANK,” American Economic Review, 108(3), 697–743.

    krueger, dirk, kurt mitman, and fabrizio perri (2016): “Macroeconomics and Household Heterogeneity,” Handbook of Macroeconomics, 2, 843–921.

    merton, robert c. (1969): “Lifetime Portfolio Selection under Uncertainty: The Continuous Time Case,” Review of Economics and Statistics, 50, 247–257.

    samuelson, paul a. (1969): “Lifetime Portfolio Selection by Dynamic Stochastic Programming,” Review of Economics and Statistics, 51, 239–46.

    summers, lawrence h. (2011): “Larry Summers and Martin Wolf on New Economic Thinking,” Financial Times interview, [http://larrysummers.com/commentary/speeches/brenton-woods-speech/](http://larrysummers.com/commentary/speeches/brenton-woods-speech/).

    yellen, janet (2016): “Macroeconomic Research After the Crisis,” Available at <https://www.federalreserve.gov/newsevents/speech/yellen20161014a.htm>.
