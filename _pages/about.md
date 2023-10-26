---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a a dual-degree senior undergraduate student at [Duke Kunshan University](https://www.dukekunshan.edu.cn/) and [Duke University](https://duke.edu/). I major in material science with physics track. My research interest lies in **quantum computing** and **quantum information**. I have no publications yet, but I have done some solid research works. 

Previous Works
======

Phase Diagram of Driven-Dissipative Bose-Hubbard Model
------

The system we study is the driven-dissipative Bose-Hubbard model with two-photon drive, one-photon loss, and two-photon loss. The effective Lindblad master equation is: 

$$H = \omega a^+ a + U a^+ a^+ a a + \lambda({a^+}^2+a^2)$$ 

$$\dot{\rho} = \mathcal{L} [\rho] = -i[H,\rho] + \kappa_1 \mathcal{D}[a] + \kappa_2 \mathcal{D}[a^2]$$ 

$$\mathcal{D}[A] = 2A\rho A^+ - A^+ A \rho - \rho A^+ A$$

where $\omega$ is the detuning, $U$ is the Kerr non-linearity, $\lambda$ is the two photon drive, $\kappa_{1,2}$ are the one-photon and two-photon loss.

By mean-field analysis and stability analysis, we find two steady state solutions $\alpha_{0,1}$ of the model. The figure plots the region where $\|\alpha_0\|^2$ is stable (red), $\|\alpha_1\|^2$ is stable (yellow), and both of them are stable (orange).

Some interesting things we find about this model:
* The steady states we get are:
  
  $$|\alpha_0|^2 = 0$$
  
  $$|\alpha_1|^2= \frac{-\kappa_1\kappa_2-\omega U + \sqrt{4\lambda^2(\kappa_2^2 + U^2)-(\kappa_1U-\kappa_2\omega)^2}}{2\kappa_2^2 + 2U^2}$$
* If $\kappa_2 = 0$, the boundary of red region on the negative side will become horizontal.
* If $\kappa_1 = 0$, two tips of the yellow region will form a sharp angle and contact.
* If we fix $\lambda$ and control $\omega$, we will see a second-order phase transition on the positive side, and a first-order phase transition on the negative side.

Effects of surface roughness and molecular shapes on gas transport through size-sieving membranes
------

We study purely repulsive Lennard-Jones particles flowing through pores of membranes piled up with spheres under a pressure gradient, which is maintained by a chemical potential gradient. The gas particles fly from the upstream chamber 1 at chemical potential $\mu_1$ to the downstream chamber 2 at a lower chemical potential $\mu_2$, implemented by the dual control volume grand canonical molecular dynamics (DCV-GCMD) method.

![model1](/images/model_1.png)

Real membranes are formed by atoms or molecules with rough surfaces that are different from ideal smooth surfaces. We approach the problem by taking into account the back reflection fraction f (ratio of particles bouncing back) caused by the bumps of rough pores. We apply multiple linear regression and found that:

$$f(\sigma_m,\sigma,n,L) = f_0[1-\exp(-k\frac{L}{\sigma_m})]\exp(-C_1\frac{\sigma}{\sigma_m}-C_2\frac{\sigma^2}{\sigma_m^2}-C_0 n)$$

where $f_0$, $C_0$, $C_1$, $C_2$, $k$ are fitting parameters, $\sigma$ is the size of gas particles, $\sigma_m$ is the size of membrane particles, $n$ is the size of pores (number of membrane particles removed along pore diameter), and $L$ is the thickness of the membrane.

With the back reflection fraction $f$, we can calculate the diffusivity considering the roughness of membrane $D = D_s (1 − f)$, where $D_s$ means the diffusivity of particles crossing a perfectly smooth membrane. According to hindered diffusion law: $D_s = D_0 (1 − \sigma/d)^2$, where $d$ is pore diamter and the font factor $D_0$ can be estimated by the diffusivity of a point particle entering the circular opening. Then we can get: $D(\sigma/d, n, L) = D_0(1 − \sigma/d)^2 (1 − f)$.

Instruction
======
This is the front page of a website that is powered by the [academicpages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages. [GitHub pages](https://pages.github.com) is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository. This template was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) created by Michael Rose, and then extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this repository](https://github.com/academicpages/academicpages.github.io) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads! An older version of this template powers my own personal website at [stuartgeiger.com](http://stuartgeiger.com), which uses [this Github repository](https://github.com/staeiou/staeiou.github.io).

A data-driven personal website
======
Like many other Jekyll-based GitHub Pages templates, academicpages makes you separate the website's content from its form. The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.

Many of the features of dynamic content management systems (like Wordpress) can be achieved in this fashion, using a fraction of the computational resources and with far less vulnerability to hacking and DDoSing. You can also modify the theme to your heart's content without touching the content of your site. If you get to a point where you've broken something in Jekyll/HTML/CSS beyond repair, your markdown files describing your talks, publications, etc. are safe. You can rollback the changes or even delete the repository and start over -- just be sure to save the markdown files! Finally, you can also write scripts that process the structured data on the site, such as [this one](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) that analyzes metadata in pages about talks to display [a map of every location you've given a talk](https://academicpages.github.io/talkmap.html).

Getting started
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the academicpages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring academicpages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
