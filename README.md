# D-Lab R CPH Workshop

[![D-Lab DataHub](https://img.shields.io/badge/launch-D--Lab%20datahub-blue)](https://dlab.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Fdlab-berkeley%2FR-CPH-Workshop&urlpath=tree%2FR-CPH-Workshop%2Flessons%2F01_introduction.ipynb&branch=main)

This repository contains the materials for D-Lab's 90-minute R Workshop for CPH.

Check out D-Lab’s [Workshop Catalog](https://dlab-berkeley.github.io/dlab-workshops/) to browse all workshops, see what’s running now, and review prerequisites.

# Workshop Goals

This is a lightweight module aimed to provide a brief introduction to R. Topics include:
- Introduction to R;
- Navigating Jupyter Notebooks;
- Variable assignment;
- Data structures;
- Working with data frames in R.

No prior experience with R is required.

## Installation Instructions

RStudio is a software commonly used by R practitioners to develop code in R. We will use RStudio to go through the workshop materials, which requires the installation of both the R language and the RStudio software. The steps to install both are below, and screenshots are available [here](https://docs.google.com/document/d/1cZEhaytG5MqLirN2Dw-Kt8VfNw9m6sL0T4yMWGnjEzk/edit?usp=sharing): 

1.  [Download R](https://cloud.r-project.org/): Follow the links according to the operating system you are running. You will first need to click on a link corresponding to your operating system, and then an additional link to select a specific version of R. Download the package, and install R onto your computer. You should install the most recent version (at least version 4.1).

    -   If you are using a Mac, click "Download R for macOS" and then select the right version of R. You will need to select the version corresponding to your specific version of macOS, as well as whether you have an Intel or Apple Silicon Mac.
    -   If you are using Windows, click "Download R for Windows", then click "base", and click the download link.
    -   If you are using Linux, click on the link corresponding to your Linux distribution, and then follow the instructions.

2.  [Download RStudio](https://rstudio.com/products/rstudio/download/#download): Install RStudio Desktop. This should be free. Do this after you have already installed R. The D-Lab strongly recommends an RStudio edition of 2022.02.0+443 "Prairie Trillium" or higher.

    -   Some individuals with older operating systems may run into odd issues. If you are running into issues with the installation of RStudio, you may need to install a specific version of RStudio. Please check [this link](https://www.rstudio.com/products/rstudio/older-versions/) if this applies to you.

3.  Download these R Fundamentals [workshop materials](https://github.com/dlab-berkeley/r-cph-workshop):

    -   Click the green "Code" button in the top right of the repository information.
    -   Click "Download Zip".
    -   Extract this file to a folder on your computer where you can easily access it (we recommend Desktop).

4.  Optional: if you're familiar with `git`, you can instead clone this repository by opening a terminal and entering `git clone git@github.com:dlab-berkeley/r-cph-Workshop.git`.

## Is R not working on your laptop?

If you do not have R installed and the materials loaded on your workshop by the time it starts, we *strongly* recommend using the UC Berkeley DataHub to run the materials for these lessons. You can access the DataHub by clicking the following button:

[![D-Lab DataHub](https://img.shields.io/badge/launch-D--Lab%20datahub-blue)](https://dlab.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Fdlab-berkeley%2FR-CPH-Workshop&urlpath=tree%2FR-CPH-Workshop%2Flessons%2F01_introduction.ipynb&branch=main)

Some users may have to click the link twice if the materials do not load initially. If you have used DataHub for another class, double check that the URL is dlab.datahub and not another department's DataHub.  

The DataHub downloads this repository, along with any necessary packages, and allows you to run the materials in an RStudio instance on UC Berkeley's servers. No installation is needed from your end - you only need an internet browser and a CalNet ID to log in. By using the DataHub, you can save your work and come back to it at any time. When you want to return to your saved work, go straight to [DataHub](https://dlab.datahub.berkeley.edu), sign in, and click on the `R-CPH-Workshop` folder.

## Run the Code

Now that you have all the required software and materials, you need to run the code.

1.  Launch the RStudio software.

2.  Use the file navigator to find the R-Fundamentals folder you downloaded from Github. Open `01_introduction.md` by double clicking on the file.

Warning: if you're opening a .Rmd file for the first time in RStudio you may be prompted to install the `rmarkdown` package. Click install and wait for it to install (RStudio might need to re-start). 

4.  Place your cursor on a given line and press `Command + Enter` (Mac) or `Control + Enter` (PC) to run an individual line of code.

5.  The `solutions` folder contains the solutions to the challenge problems.

# Additional Resources

Check out the following online resources to learn more about R:

* [Software Carpentry](https://swcarpentry.github.io/)
* [Quick-R](http://statmethods.net/)  
* [UCLA idre](https://stats.idre.ucla.edu/r/)  
* [R-bloggers](https://www.r-bloggers.com/)  
* [R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/)
* [The tidyverse style guide](http://style.tidyverse.org/)
* [Quick Intro to Parallel Computing in R](https://nceas.github.io/oss-lessons/parallel-computing-in-r/parallel-computing-in-r.html)

as well as the following books:

* [Bookdown Featured Books](https://bookdown.org/)  
* [Kearns GJ. 2010. Introduction to Probability and Statistics in R](http://www.atmos.albany.edu/facstaff/timm/ATM315spring14/R/IPSUR.pdf)
* [Wickham H. 2014. Advanced R](http://adv-r.had.co.nz/)  
* [R for Data Science](http://r4ds.had.co.nz/)  
* [Lander J. 2013. R for everyone: Advanced analytics and graphics](http://www.jaredlander.com/r-for-everyone/)  
* [Matloff N. 2011. The art of R programming: A tour of statistical software design](https://www.nostarch.com/artofr.htm)  
* [Brunsdon C, Comber L. 2015. An Introduction to R for Spatial Analysis and Mapping](https://us.sagepub.com/en-us/nam/an-introduction-to-r-for-spatial-analysis-and-mapping/book241031)
* [James G, Witten D, Hastie T, Tibshirani R. 2013. An Introduction to Statistical Learning: With Applications in R, 7th edition](http://faculty.marshall.usc.edu/gareth-james/ISL/)

# About the UC Berkeley D-Lab

D-Lab works with Berkeley faculty, research staff, and students to advance data-intensive social science and humanities research. Our goal at D-Lab is to provide practical training, staff support, resources, and space to enable you to use R for your own research applications. Our services cater to all skill levels, and no programming, statistical, or computer science backgrounds are necessary. We offer these services in the form of workshops such as R Fundamentals, one-to-one consulting, and working groups that cover a variety of research topics, digital tools, and programming languages.

Visit the [D-Lab homepage](http://dlab.berkeley.edu/) to learn more about us. View our [calendar](http://dlab.berkeley.edu/calendar-node-field-date) for upcoming events, and also learn about how to utilize our [consulting](http://dlab.berkeley.edu/consulting) and [data](http://dlab.berkeley.edu/data-resources) services. 

# Other D-Lab R workshops

Here are other R workshops offered by the D-Lab:
## Basic Competency
* [R Data Wrangling](https://github.com/dlab-berkeley/R-Data-Wrangling)
* [R Graphics with ggplot2](https://github.com/dlab-berkeley/R-graphics)
* [R Functional Programming](https://github.com/dlab-berkeley/R-functional-programming)
* [Geospatial Fundamentals in R with sf](https://github.com/dlab-berkeley/Geospatial-Fundamentals-in-R-with-sf)
* [Census Data in R](https://github.com/dlab-berkeley/Census-Data-in-R)

## Intermediate/Advanced Competency
* [Unsupervised Learning in R](https://github.com/dlab-berkeley/Unsupervised-Learning-in-R)
* [R Machine Learning with tidymodels](https://github.com/dlab-berkeley/Machine-Learning-with-tidymodels)
* [Introduction to Deep Learning in R](https://github.com/dlab-berkeley/Deep-Learning-in-R)
* [Fairness and Bias in Machine Learning](https://github.com/dlab-berkeley/fairML)
* [R Package Development](https://github.com/dlab-berkeley/R-package-development) 

# Contributors
* [Pratik Sachdeva](https://github.com/pssachdeva)
* [Tom van Neunen](https://github.com/tomvannuenen)
