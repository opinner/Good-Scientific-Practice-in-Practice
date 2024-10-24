# Good Scientific Practice — in Practice

> [!IMPORTANT]  
> This is a copy of an ongoing work in my current research project.
> The vast majority of this work was written by me, but single links were recommended by other project members.
> It is copied here to make it available to people outside the project and also to connect it publicly with my name. 

## Introduction

This document curates (digital) resources to various topics. In their sum, these resources describe something like *Good Scientific Practice*. The idea is to ease the entry into climate research. But this implies by no means that experienced climate researchers always follow good scientific practice. Some do it more, some do it less. 

This document presents a wide range of content, from the very basics of scientific programming to heavily specialized references, which are much more difficult to find from a simple google search. 

Many things are linked in this document, but every resource is marked by an emoji, which also signals an estimate for the time it takes to work through it and learn how to use it. The effort is categorized as ⏱️ (*Short)*, ⌛ *(Medium)* or 🕰️ *(Long)*. With a great deal of interpretation, they could mean (*minutes), (hours), *or* (days), *but this is guaranteed to be inaccurate. 

If you are a new PhD student, your main task is to fill in the Topic Wish list. If you have specific questions, write an email to anyone on the contributor list, at least they can point you to the right direction/person. Although there is some text written already, this is a work in progress and multiple sections are very short or even completely empty. They will be hopefully filled in the future. Requesting a certain topic should in the best case accelerate that process.

Everybody else should make their knowledge available. Feel free to change or add anything in this document, including titles, structure, and text, especially if you think you can explain it better or know a better resource. But maybe explain your change in a comment, if the Why is not obvious. Because a nondescript list of links is basically useless, each resource should come with an explanation (between a short sentence to a paragraph) and be marked with the effort it requires (⏱️, ⌛, 🕰️). And at last, add your name to the list of contributors.

This document was conceptualized at the [TRR181](https://www.trr-energytransfers.de/) retreat 2024.

## Tables of Content 

- [Introduction](#introduction)
- [Topic Wish list](#topic-wish-list)
- [Programming](#programming)
  * [The Basics](#the-basics)
    + [Courses](#courses)
    + [Self-teaching](#self-teaching)
    + [Integrated Development Environments (IDEs)](#integrated-development-environments--ides-)
    + [Version Control with git](#version-control-with-git)
  * [Scientific Programming](#scientific-programming)
    + [Python](#python)
    + [Miscellaneous tips, taken from experience](#miscellaneous-tips--taken-from-experience)
  * [High Performance Computing](#high-performance-computing)
  * [Machine Learning](#machine-learning)
  * [Code Documentation](#code-documentation)
- [Writing](#writing)
  * [General Tips](#general-tips)
  * [LaTeX](#latex)
- [Communication & Publication](#communication---publication)
  * [Visualization](#visualization)
  * [Publication in Journals](#publication-in-journals)
  * [Code & Data publication](#code---data-publication)
    + [Make your work citable](#make-your-work-citable)
- [Managing your Science](#managing-your-science)
  * [Citation Management](#citation-management)
  * [Time Management](#time-management)
  * [(Digital) Note-Taking](#-digital--note-taking)
- [Misconduct — What to do?](#misconduct---what-to-do-)
  * [Bad Scientific Practice](#bad-scientific-practice)
  * [Interpersonal/Sexual Misconduct](#interpersonal-sexual-misconduct)
- [List of TRR-specific resources](#list-of-trr-specific-resources)

## Programming


### The Basics


#### Courses 

Information about the course done by Jörn Behrens at the University of Hamburg will follow. Other courses done by the TRR will very likely not be basic but focus on programming skills specific to the TRR, which cannot easily be found offered by others, such as working with climate model data. For a list of already existing TRR-specific resources, go to the end of this document to see the [List of TRR-specific resources](#list-of-trr-specific-resources-14).

Basic (and even advanced) programming courses are offered by many institutes and organisations, for example by the German *Helmholtz association* ([Helmholtz HiDA Course Catalog](https://www.helmholtz-hida.de/course-catalog/en/)). The (currently) next introductory course is the 1-day online course 🕰️ [HIDA Kickstart Python](https://events.hifis.net/event/1310/), happening on Thursday, October 10, 2024, 9 am to 5 pm. The registration is already open. 

A worldwide provider of courses is *Software Carpentry*, see their [Upcoming Workshops](https://software-carpentry.org/workshops/upcoming/).


#### Self-teaching

🕰️ [All written lessons from Software Carpentry](https://software-carpentry.org/lessons/) are a good starting point. Specific lessons of them will also be referenced in the upcoming paragraphs. 

🕰️ [Workshop Materials ](https://hifis.net/services/software/training#workshop-materials)from the Helmholtz Digital Services for Science are freely available and cover many introductory topics. 


#### Integrated Development Environments (IDEs)

An IDE is simply said anything you can write code in that does more than a text editor. While code written in the latter is usually run from a terminal, an IDE combines code writing and execution, while also allowing for auto-completion, debug mode and automated checking of your source code for programmatic and stylistic errors (called *linting*).

Very common programs are [Visual Studio Code](https://code.visualstudio.com) or [PyCharm](https://www.jetbrains.com/pycharm/) (for python), but many other software products exist. One can even extend powerful text editors like vim to function as an IDE. As a proprietary language, Matlab comes with its own specialized coding environment. 

[Jupyter Labs or Jupyter Notebooks](https://docs.jupyter.org/en/latest/) provide cell-based code execution. Often used with python, coding in Julia, R and even Matlab and Sage is also possible. This approach is especially useful for explorative work, where the effect of small changes to the code can immediately be looked at. 

Jupyter Notebooks can also be executed in [Google Colab](https://colab.research.google.com/), an online, collaborative service in the browser. It therefore acts like GoogleDocs for executable code. Take a look at their [FAQs](https://research.google.com/colaboratory/faq.html) for more information. 


#### Version Control with git

Version control means you are not just saving the current state of a file, but also all changes to it, together with the information of who did what at which time. This allows practically infinite redos as you are able to return to any state your file was previously in. 

The most commonly used program to do that is git. It is usually connected to a so-called repository on a cloud storage service, such as GitHub, GitLab or bitbucket. Despite the possibility of git to be quite complicated from time to time, one can get pretty far by repeatedly using just 3 commands:


<table>
  <tr>
   <td><code>git add</code>
   </td>
   <td>Tell git to remember the changes you’ve made to files.
   </td>
  </tr>
  <tr>
   <td><code>git commit</code>
   </td>
   <td>Save those changes, together with a message explaining what you did.
   </td>
  </tr>
  <tr>
   <td><code>git push</code>
   </td>
   <td>Send the saved changes to a remote place like GitHub
   </td>
  </tr>
</table>


Before and after every step, you can use `git status` to check what git is currently doing. 

If you use an Integrated Development Environment (IDE), these commands are often replaced by a graphical user interface, which makes it more accessible for beginners. `git pull` is the opposite to `git push` and will download changes from a remote place. This is essential if there are changes made by others and less so if only you alone work on your code. 

A short introduction to immediately start working with Python, git and GitHub is ⏱️ [Set up your project — Good research code](https://goodresearch.dev/setup). A more detailed and easy to understand explanation on what git is, why it is useful and how do you use it, is given in ⌛ [Software Carpentry — Version Control with Git: Summary and Setup](https://swcarpentry.github.io/git-novice/). 

But on a day-to-day basis, almost no one remembers the exact git commands for anything even slightly complicated. Whenever you try something new, did anything you regret or get an error, look up the ⏱️ [git-flight-rules](https://github.com/k88hudson/git-flight-rules) to find an answer to most common problems. With this, you don’t have to understand git in all its complexity and are still able to do everything you want.

⌛[Oh My Git!](https://ohmygit.org/) provides a (free) training game for git. The first few levels cover all the commands for basic git use. 

⌛ [A Concise Introduction to Git for Academics](https://bitbucket.org/marcel_oliver/git_for_academics/src/master/README.md) was written by TRR member Marcel Oliver and includes how to connect git to bitbucket, the use of git in a collaborative setting and the possible solutions to more advanced git problems. 

Since the current MATLAB version 2024b, using git is now less complicated than before, but apparently still complicated:



* ⌛ [Set Up Git Source Control in MATLAB](https://de.mathworks.com/help/matlab/matlab_prog/set-up-git-source-control.html)
* ⌛ [Use Git in MATLAB](https://de.mathworks.com/help/matlab/matlab_prog/use-git-in-matlab.html)

Together with thinking about which files you want to track and save, one should also think about which files should definitely not be tracked to not clutter the repository. The rules for that are saved in a file named *.gitignore*. A list of typical rules, dependent on the programming language of choice, can be taken from this ⏱️ [collection of useful .gitignore templates](https://github.com/github/gitignore). But these do not take into account the usual files existing in scientific work, like data sets of various file types and figures, etc. Therefore, one should always adapt the ignore rules to their own use case to keep the repositories tidy.


### Scientific Programming

The [FAIR Principles for Research Software](https://doi.org/10.15497/RDA00068) stand for 



* **Findable**: Software should be easy to locate, whether you're searching in a repository or on the web. This means using clear and unique identifiers (like a DOI) and detailed descriptions, so people can find it quickly.
* **Accessible**: Once found, the software should be easy to access, even if you need to log in or request permission. Clear instructions should guide how to get or use the software, and it should remain accessible over time.
* **Interoperable**: The software should work well with other software, systems, or data. This means using standard formats and well-documented code so different tools and platforms can easily understand and use it.
* **Reusable**: The software should be easy to reuse for new purposes. This requires good documentation, clear licensing, and well-structured code, so others can confidently apply it to their own research or projects.

These guidelines are useful for any officially published code, but are also good practice on just your local machine, as future-you may not remember much if you are looking at your old code again from months and years ago.  

🕰️ [Good Scientific Code Workshop](https://github.com/JuliaDynamics/GoodScientificCodeWorkshop) is a (mostly) language-agnostic workshop, meaning that the principles are about general coding. It aims to show how to write code that is “Clear, Easy to understand, Well-documented, Reproducible, Testable, Reliable, Reusable, Extendable, and Generic”. Examples and exercises are in Julia and Python.

⌛ [The Good Research Code Handbook](https://goodresearch.dev/) is a really good, short but concise write-up on how to achieve good practices in scientific python programming. It covers code organisation, version control, coding principles, code style, testing, etc. in just a few pages, while staying easy to follow. 

A ⏱️ [List of Software recommendations](https://ocean.miraheze.org/wiki/Software_recommendations) was compiled by PhD students of the 2nd TRR phase and lists software and packages in Matlab and Python, which were found to be useful. They range from general helpful to be of very niche purpose.


#### Python 

⌛ [Introduction to the SciPy Stack - Scientific Computing Tools for Python](https://mids.ku.de/oliver/teaching/scipy-intro/scipy-intro/scipy-intro.html), written by TRR member Marcel Oliver, is especially suited for easing the migration from Matlab to python. 

The written course 🕰️ [Working with Spatio-temporal data in Python](https://annefou.github.io/metos_python/) introduces common data types in climate sciences, such as netCDF, HDF and GeoTIFF, and how to work with them.

For plotting data defined on geographical coordinates, the package [cartopy](https://scitools.org.uk/cartopy/docs/v0.16/index.html#) is often used. 

⌛ [Introduction to Cartopy - Part 1](https://github.com/opinner/Articles/blob/main/Articles/Introduction_to_Cartopy_Part1.ipynb) and ⏱️ [Hill shading and IBSCO data in Python](https://github.com/opinner/Articles/blob/main/Articles/IBSCO_data_in_Python.ipynb) show more examples than the official gallery on the cartopy website. By accessing their GoogleColab counterparts, they can even be run interactively. 

The repository to the ⌛ [tapgfd workshop](https://gitlab.dkrz.de/u241317/tapgfd_workshop/), developed for a recent conference by TRR-members Moritz Epke and Pablo Sebastia Saez, introduces general python visualization concepts for regular gridded datasets (e.g. on 2D time series, idealized models), but also for datasets from unstructured grids (such as ICON and FESOM).


#### Miscellaneous tips, taken from experience



* Regardless of the language, most collections of tips for scientific or just general programming boil down to:
    * Give variables meaningful names
    * Comment not what your code does, but why it does that
    * Split your program in easier to understand parts, by using functions, classes, modules. 
* [ChatGPT](https://chatgpt.com/) is a great tool/conversational partner to get code you don’t understand explained.
* Visualization is often the intermediate and end step of scientific programming. See the section about [Visualization](#visualization-10) for tips.
* Connect each generated figure to the script responsible for it, by adding a watermark/footnote to the figure or by following a naming scheme, derived from the script name. If not, there will be a time when you don't remember how a certain figure was made. 
* Following a style guide of your language like the [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html) will make your code easier to read for others. 
* Multiple institutions in Germany offer free software consulting for scientists, such as [Software Engineering Consulting](https://www.hifis.net/services/software/consulting.html) by HIFIS or [Services and Consultancy](https://www.dkrz.de/en/services) by the DKRZ.


### High Performance Computing

Institutions, who offer high-performance computing time, usually also offer regular courses on how to work in these environments. For Germany, look at the following schedules:



* [Courses and Workshops at the National High Performance Computing Germany](https://www.nhr-verein.de/en/courses-and-workshops)
* [Trainings/Workshops: Gauss Centre for Supercomputing e.V.](https://www.gauss-centre.eu/trainingsworkshops)
* [Training courses for users — Jülich Supercomputing Centre (JSC)](https://www.fz-juelich.de/en/ias/jsc/education/training-courses)
* [Helmholtz HiDA Course Catalog](https://www.helmholtz-hida.de/course-catalog/en/) 

International addresses are



* [HPC Carpentry](https://www.hpc-carpentry.org/), also useful for self-teaching with their 🕰️ [Community Developed Lessons](https://www.hpc-carpentry.org/community-lessons/#hpc-carpentry) 
* [Events and Training from LUMI](https://lumi-supercomputer.eu/events/), a supercomputer centrum in Finland. 
* [Versatile training at the Finnish IT Center for Science](https://www.csc.fi/training#training-calendar)

The write-up 🕰️ [Python on Levante](https://pad.gwdg.de/GSW4dgHZSGm6KUev6mQcdw?view) explains how to code in python on the [Levante HPC System](https://docs.dkrz.de/doc/levante/index.html), the latest super computer of the[ ](https://docs.dkrz.de)German Climate Computing Centre (DKRZ). But it also contains widely applicable knowledge on how to set up the IDE VS Code, coupling with AI (coding with Copilot), parallelization strategies (e.g. mpi4py or dask slurm cluster) and workflow improvements (e.g. document your results on your own webpage).


### Machine Learning

To understand how neural networks and machine learning works, a great series of explanations can be found in the 🕰️ [Playlist about Neural networks by 3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi). It combines great (maybe the best)  visualizations and easy to understand explanations with a minimum of presupposed knowledge. But it still manages to go deep into the topic in the course of the series. The (currently) 7 videos range between 10 and 27 minutes in length.

From a workshop in the 2nd TRR phase, a ⏱️ [TRR 181 ML Tutorial](https://colab.research.google.com/drive/1t3bWaDxzipdLfGgr6q_w05ys1Y8aUdZw?usp=sharing) remains executable in google colab. It is a very gentle, low-level introduction and even covers basic python syntax to be as easy to understand as possible. This tutorial does not go far, but provides a simple toy example, which can be interactively tinkered with. 


### Code Documentation


## Writing


### General Tips

Regardless of the text editor, a good grammar and typography checking tool can significantly reduce small errors you have in your writings. 

[LanguageTool](https://languagetool.org/?force_language=1) is a free tool, with extensions for common text editors. Its browser-based version allows spellchecking in all text you write in your browser, for example in emails or collaborative text editors such as Google Docs or Overleaf.  


### LaTeX

LaTeX is a type-setting software, often used in the academic world for long texts with a complicated structure, like theses, or for publications containing many mathematical expressions. But the wide-spread use also caused many other programs to emulate LaTeX or at least allow for a very similar syntax for writing equations. Nowadays, mathematical commands, originally from LaTeX, can be used in Word, Markdown, HTML, etc. 

⏱️ [A Very Short Introduction to LaTeX](https://dl.icdst.org/pdfs/files3/f6a19402d10da1c25e4740651a7c0aa1.pdf) is a useful start if one has never seen or used any LaTeX. It references 🕰️[The Not So Short Introduction to LaTeX](https://tobi.oetiker.ch/lshort/lshort.pdf), also titled *LaTeX in 280 minutes*, an extensive, up-to-date introduction to everything concerning LaTeX. 

An easy entry to LaTeX is provided by the online editor [Overleaf](https://www.overleaf.com). But recent changes made it almost impossible to use it on a free plan, and the TRR lost its way of funding a premium version. But if you achieve to get a premium licence from your local institute or university, Overleaf is still a very convenient tool, especially for collaborative writing.

Most journals provide a template, which must only be filled in and does not require any LaTeX knowledge except the very basics.

⏱️ [Detexify](https://detexify.kirelabs.org/) recognizes drawings of symbols and gives out the correspondent LaTeX commands. This approach usually finds LaTeX symbols quicker than looking through the documentations. 


## Communication & Publication


### Visualization

⏱️ [Friends Don't Let Friends Make Bad Graphs](https://github.com/cxli233/FriendsDontLetFriends) discusses various types of data visualizations that should be avoided, such as bar plots for mean separation and pie charts, explaining why they are misleading or ineffective in accurately representing data.

The University of Texas provides ⌛ [Design strategies for scientific figures](https://utexas.app.box.com/s/rbjcse706hehctt9aw5xjb84hq6ycayu), with many rules of thumb and examples of how to improve scientific figures of different types. All strategies are summarized to a single page in their ⏱️[Design Tips for Scientists Checklist](https://utexas.app.box.com/s/8djs9jikr311t54upxixvgac85j21rfe). 

If you want to use a good color map, but do not know which one, ⏱️ [cmocean](https://matplotlib.org/cmocean/) is always a good first address. Its suggestions for color maps commonly used oceanographic variables are (at least) available in Python, Matlab, R and Julia and are easy to import and use.

Custom discrete color maps can be generated by [Colorgorical](http://vrl.cs.brown.edu/color). Also useful for qualitative color maps, where the color ist just for distinction and not for an extra numerical dimension.

If scientific figures are created in vector-based formats such as SVG or PDF, they can be opened in vector graphics editors such as [Inkscape](https://inkscape.org/) (which is free and open-source) and every individual part or layer of the figure remains accessible and changeable. If you cannot easily create a figure as perfect as you like in your code directly, some post-processing in graphic programs may be way faster than fiddling with the code. 


### Publication in Journals

For the right selection of a journal to publish in, you can orient yourself on the journals you read from the most during the literature research. Asking your potential co-authors is also good, as they may a suitable suggestion. 

Avoid predatory journals by checking them before in the [Beall's List of Potential Predatory Journals and Publishers](https://beallslist.net/). But the list itself is not without criticism, and alternative lists exists. See [Beall's List - Wikipedia](https://en.wikipedia.org/wiki/Beall%27s_List) for more information. 

On the website of [Sherpa Services](https://beta.sherpa.ac.uk/), you can look up copyright rules for every scientific journal and any potential embargo you have to follow until your work can be republished. These can range from 0 months to 24 months. Long embargoes could be a problem for a cumulative PhD thesis, as this is practically a republication. 


### Code & Data publication

🕰️ [The Turing Way](https://book.the-turing-way.org/) says about itself that it is “a handbook to reproducible, ethical and collaborative data science.” Although this book starts with the basics, it exceeds them quickly. The scope of the contents is too extensive to be summarized here shortly. 


#### Make your work citable

[Zenodo](https://zenodo.org/), developed and managed by CERN, and[ figshare](https://figshare.com/) by Springer Nature are two free ways to publish more than the written part of your results, especially your code. Introductions are for example given in 



* ⏱️ [Referencing and citing GitHub content with Zenodo](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content) 
* ⏱️ [How to set metadata for a DOI record on Zenodo](https://github.com/castelao/inception)

A small example for the publication of code from a TRR member can be found under the DOI (Digital Object Identifier) [10.5281/zenodo.13350486](https://doi.org/10.5281/zenodo.13350486), based on the GitHub repository [opinner/Pinner_et_al_2024](https://github.com/opinner/Pinner_et_al_2024). A bigger example is the entirety of FESOM 2.0 under [10.5281/zenodo.161319](https://doi.org/10.5281/zenodo.161319). 

Another possibility to publish outside journals would be[ the Open Science Framework](https://osf.io/) (but of which I ([OP](#contributors-2)) know nothing about). For publishing data sets, especially[ Pangaea](https://www.pangaea.de/), (a Data Publisher specially for Earth & Environmental Science) and [figshare](https://figshare.com/), are well-suited services.

For some research areas (including math and physics), [arXiv ](https://arxiv.org/)is the primary preprint server. It also allows limited support for ancillary files such as code. For details, see here: [ancillary files in arXiv](https://info.arxiv.org/help/ancillary_files.html). An alternative is [EarthArXiv](https://eartharxiv.org/), which is specialized to publications from earth system science. 


## Managing your Science


### Citation Management

Part of science is being aware of and referencing previous work, aka the “state of the art”. To keep the unlimited numbers of paper organized, citation management is necessary. The most popular choices are[ Zotero](https://www.zotero.org/),[ Mendeley](https://www.mendeley.com/search/), [Citavi](https://www.citavi.com) and[ JabRef](https://www.jabref.org/). 

Zotero is a free and open source tool, which supports many additional plugins for more capabilities. An example for how to set up Zotero and use it with LaTeX is described in the blog post[ ](https://gunnarvoet.github.io/post/zotero/)⏱️ [Publication Management with Zotero](https://gunnarvoet.github.io/post/zotero/). Examples for useful plugins are:



* [Zotero | Connectors](https://www.zotero.org/download/connectors) Browser plugin to directly import new references
* [word_processor_integration](https://www.zotero.org/support/word_processor_integration) plugin to Microsoft Word
* [better-bibtex](https://retorque.re/zotero-better-bibtex/citing/) Better citation keys for exports to BibTeX
* [ZotFile](http://zotfile.com/) Better management of attachments, mostly pdfs

If you work with[ the online LaTeX editor Overleaf](https://www.overleaf.com), you can directly ⏱️ [connect a project to your Zotero account](https://www.overleaf.com/learn/how-to/How_to_link_your_Overleaf_account_to_Mendeley_and_Zotero) to avoid manually uploading and updating a *.bib* file.


### Time Management


### (Digital) Note-Taking

[Notion](https://www.notion.so/) is one of the better ones on the market with a powerful free tier. The danger is you spend too much time organizing the records instead of making the records.

[Obsidian:](https://obsidian.md/) Different approach to note-taking — all is done in Markdown. Has a powerful plugin system that allows you to do even mind maps. All files can be saved locally, so no connection to the web is necessary. In its simplest setup, it is immediately elegant, easy, and well organized and therefore useful. But with its potential complexity and customizability, it shares the same danger with Notion, that organizing may take up more time than writing.

The ⏱️ [tutorial for python on Levante](https://pad.gwdg.de/GSW4dgHZSGm6KUev6mQcdw?view#35-build-documentation) is an example for a documentation written in Markdown, with a very short explanation on how to do it. The webpage (hosted on levante itself) is written in Markdown and assembled using sphinx. Once set up, it is an easy and fast way to share/show your results. It allows keeping track of your key results by collecting them on your own webpage. 


## Misconduct — What to do?

For any scientific or personal misconduct, experienced or observed inside the TRR181 and its associates, you can follow the following guide to what steps are possible and how the TRR will react to complaints. Just asking for advice is also always possible.


### Bad Scientific Practice

If good scientific practice exists, there must also be some kind of opposite. If you see bad science, and you believe it to be accidental, talk to the person directly. In the case you think the bad scientific practice is purposely neglectful or even malicious, you should talk to research ombudspeople. Every institute/department/university should have people assigned to this role. The highest address in Germany for complaints is the [Ombuds Committee for Research Integrity in Germany](https://ombudsman-fuer-die-wissenschaft.de/?lang=en).

The most common examples are



* results are not correctly attributed to the responsible person
* results are selectively presented and mislead how the full picture looks like


### Interpersonal/Sexual Misconduct

⌛ [It's not that grey — How to identify the grey area — a practical guide for the twilight zone of sexual harassment](https://www.sarahassan.at/wp-content/uploads/2023/11/Its-not-that-Grey_Period_Guide_2019_online.pdf), or also the ⌛ [German Version](https://www.sarahassan.at/wp-content/uploads/2023/11/Grauzonen-gibt-es-nicht_Hassan-Sanchez-Lambert.pdf). 

People on fieldwork are statistically more likely to experience harassment. 


## List of TRR-specific resources

* The write-up 🕰️ [Python on Levante](https://pad.gwdg.de/GSW4dgHZSGm6KUev6mQcdw?view) explains how to code in python on the [Levante HPC System](https://docs.dkrz.de/doc/levante/index.html), the latest super computer of the[ ](https://docs.dkrz.de)German Climate Computing Centre (DKRZ). But it also contains widely applicable knowledge on how to set up the IDE VS Code, coupling with AI (coding with Copilot), parallelization strategies (e.g., mpi4py or dask slurm cluster) and workflow improvements (e.g., document your results on your own webpage).
* The repository to the ⌛ [tapgfd workshop](https://gitlab.dkrz.de/u241317/tapgfd_workshop/), developed for a recent conference by TRR-members Moritz Epke and Pablo Sebastia Saez, introduces general python visualization concepts for regular gridded datasets (e.g., on 2D time series, idealized models), but also for datasets from unstructured grids (such as ICON and FESOM).
* A ⏱️ [List of Software recommendations](https://ocean.miraheze.org/wiki/Software_recommendations) was compiled by PhD students of the 2nd TRR phase and lists software and packages in Matlab and Python, which were found to be useful. They range from general helpful to be of very niche purpose.





If this document exceeds a certain length, I ([OP](#contributors-2)) would propose a switch from a linear to a wiki structure. Either by merging it into my own knowledge transfer side project [OceanAtmosWiki](https://ocean.miraheze.org/wiki/Main_Page) (probably not so smart) or by using [GitHub Wiki](https://docs.github.com/en/communities/documenting-your-project-with-wikis/about-wikis), which would even allow the incredibly easy use of Markdown for formatting code, graphs, etc. It would also make this document independent of my own Google account and allow for officially documented contribution, useful for the CV and personal profile. But that is a discussion necessary only in the case of wide success. 
