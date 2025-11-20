![Version](https://img.shields.io/static/v1?label=elfeedorg&message=0.1&color=brightcolor)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)


# Blaine's elfeed.org file of RSS feeds of interest

Elfeed is a package for the highly customizable text editor Emacs.
This package provides an interface to the most recent current contents of selected journals.
Elfeed provides direct links to each article for further exploration.
Elfeed spares you of the trouble of visiting the current contents of each journal to find papers of interest.
This form of literature searching compliments keyword or topic-driven searches.
You might not have considered certain terms to be relevant when they would be required to be able to retrieve literature that is relevant to your interests.

This repository contains my source file, elfeed.org, that has all the URLs to the RSS feeds of the journals that I follow.
Obviously, this file is written in the org-mode typesetting language.
Org-mode is very convenient for the creation and management of hierarchical lists.
Subtrees within the list can be shuffled up or down.
Org-mode also supports the folding of topics.

The main kind of feed that I follow are the current contents of journals.
Some other kinds of websites with RSS feeds inlcude blogs, YouTube channels, forums, databases, and GitHub features like releases.

This collection of RSS feeds is driven by my research needs and interests. 
My interests include the following:

- Biochemistry
- Molecular Biology
- Parasitology
- Cancer Biology
- Protein Structure
- RNA structure
- RNA editing
- Biomolecular Crystallography
- Biological Quantum Crystallography
- Biological Small Angle Scatering
- Structure based Drug Design
- Moleciular Graphics
- Molecular Simulations
- Tools to assist with writing computer code
- Literate programming
- Computational Notebooks
- Reproducible research
- Classic and Modern Design of Experiments
- Bayesian Data Analysis
- Emacs
- Clojure

If you have overlapping interests, you may want to copy the relevant entries because the gathering of the URLs for these feeds was time consuming.
Usually a RSS icon is clicked to toke you to another tab with the RSS code.
If the RSS icon is absent, visuallize the source code of the HTML file and search for `RSS`. 
It will be next or part of a the URL for the RSS feed.

In the elfeed.org file, the feeds are organized by publisher because each publisher has their own style of formatting the URL.
This approach to organizing the feeds supports more rapid deduction of the appropriate URL address.

To interface the elfeed.org file with elfeed, you need to install the package elfeed-org.
This is the configuration that I use in my init.el file:

```elisp
;; List the feeds in an org file here:
(use-package elfeed-org
  :after elfeed
  :custom
  (rmh-elfeed-org-files
   (list "~/e30fewpackages/elfeed.org"))
)
```

I am using the configuration for elfeed that I found [here:](https://plrj.org/2025/06/14/my-emacs-elfeed-configuration/).

Run the following commnds in the minibuffer to transfer the feeds from elfeed-org to elfeed, update the feeds, and then display the feeds.:


1. M-x elfeed-org
2. M-x elfeed update
3. M-x elfeed

To do a search, enter `s`.
In the minbuffer, add `+ python`

![This is a screen shot of the results:](https://github.com/MooersLab/elfeedorg/blob/main/images/pythonFeeds.png)

The tags are in the parentheses on the right.



## Update history

|Version      | Changes                                                                                                                                                                         | Date                 |
|:-----------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------|
| Version 0.1 |   Added badges, funding, and update table.  Initial commit.                                                                                        | 11/13/2025  |
| Version 0.2 |  Changed the heirarchy in elfeedorg                                                                                                               ---------- | 11/14/2025  |

## Sources of funding

- NIH: R01 CA242845
- NIH: R01 AI088011
- NIH: P30 CA225520 (PI: R. Mannel)
- NIH: P20 GM103640 and P30 GM145423 (PI: A. West)
