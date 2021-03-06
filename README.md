<div style="float: right"><img src="./data-raw/images/discovr_hex.png" width="150"></div>

# discovr: Resources for Discovering Statistics Using R and RStudio (Field, 2021)

***
> **NOTE**: This package is incomplete but under active development. I have released it early in case it is useful for instructors needing to move rapidly to remote learning because of the current global pandemic. Check back here for updates/new tutorials.

***

The `discovr` package contains resources for my 2021 textbook [Discovering Statistics Using <img src="./data-raw/images/r_logo.png" width="18"> and <img src="./data-raw/images/rstudio_logo.png" width="48">](https://www.discoveringstatistics.com/books/discovering-statistics-using-r/). There are tutorials written using [learnr](https://rstudio.github.io/learnr/). Once a tutorial is running it's a bit like reading a book but with places where you can practice the <img src="./data-raw/images/r_logo.png" width="18"> code that you have just been taught. The `discovr` package is free and offered to support tutors and students using my textbook who want to learn <img src="./data-raw/images/r_logo.png" width="18">.

## Installing `discovr`

To use `discovr` you first need to install <img src="./data-raw/images/r_logo.png" width="18"> and <img src="./data-raw/images/rstudio_logo.png" width="48"> and familiarise yourself with <img src="./data-raw/images/r_logo.png" width="18">, <img src="./data-raw/images/rstudio_logo.png" width="48"> and good workflow practice. You can do this using [this interactive tutorial](http://milton-the-cat.rocks/learnr/r/r_getting_started/). Once you have installed <img src="./data-raw/images/r_logo.png" width="18"> and <img src="./data-raw/images/rstudio_logo.png" width="48"> you can install `discovr`. The package is in development so you have to install it from github. To install the package execute (in <img src="./data-raw/images/rstudio_logo.png" width="48">):

```
if(!require(htmltools)){
  install.packages('remotes')
}

remotes::install_github("profandyfield/discovr", dependencies = TRUE)
```

If you are trying to install on a networked computer the install might fail (it's to do install.packages not liking UNC paths, which I'm not even going to pretend to understand). The solution is to specify the location of your <img src="./data-raw/images/r_logo.png" width="18"> library at the point of install. Most networks will map network locations to a drive name (for example, at my own University, users accounts are on the 'N' drive). Find the location of your <img src="./data-raw/images/r_logo.png" width="18"> library (e.g., `N:/Documents/R/win-library/3.5`), possibly executing `.libPaths()` to help you, and specify this location using the `lib` argument:

```
remotes::install_github("profandyfield/discovr", dependencies = TRUE, lib = "N:/Documents/R/win-library/3.5")
```

## Interactive tutorials

I recommend working through [this tutorial](http://milton-the-cat.rocks/learnr/r/r_getting_started/) on how to install, set up and work within <img src="./data-raw/images/r_logo.png" width="18"> and <img src="./data-raw/images/rstudio_logo.png" width="48"> before starting the interactive tutorials.

### List of tutorials

* **discovr_01**: Key concepts in <img src="./data-raw/images/r_logo.png" width="18"> (functions and objects, packages and functions, style, data types, tidyverse, tibbles)
* **discovr_02**: Summarizing data (frequency distributions, grouped frequency distributions, relative frequencies, histograms, mean, median, variance, standard deviation, interquartile range)
* **discovr_03**: Confidence intervals: interactive app demonstrating what a confidence interval is, computing normal and bootstrap confidence intervals using R, adding confidence intervals to data summaries.
* **discovr_05**: Visualizing data. The ggplot2 package, boxplots, plotting means, violin plots, scatterplots, grouping by colour, grouping using facets, adjusting scales, adjusting positions."
* **discovr_06**: The beast of bias. Restructuring data from messy to tidy format (and back). Spotting outliers using histograms and boxplots. Calculating z-scores (standardizing scores). Writing your own function. Using z-scores to detect outliers. Q-Q plots. Calculating skewness, kurtosis and the number of valid cases. Grouping summary statistics by multiple categorical/grouping variables.
* **discovr_07**: Associations. Plotting data with GGally. Pearson's r, Spearman's Rho, Kendall's tau, robust correlations.
* **discovr_08**: The general linear model (GLM). Visualizing the data, fitting GLMs with one and two predictors. Viewing model parameters with broom, model parameters, standard errors, confidence intervals, fit statistics, significance.
* **discovr_09**: Categorical predictors with two categories (comparing two means). Comparing two independent means, comparing two related means, effect sizes.
* **discovr_10**: Moderation and mediation. Centring variables (grand mean centring), specifying interaction terms, moderation analysis, simple slopes analysis, Johnson-Neyman intervals, mediation with one predictor, direct and indirect effects, mediation using lavaan.


### Running a tutorial

In <img src="./data-raw/images/rstudio_logo.png" width="48"> Version 1.3 onwards there is a tutorial pane. Having executed

```
library(discovr)
```

A list of tutorials appears in this pane. Scroll through them and click on the <img src="./data-raw/images/start_tutorial.png" width="64"> button to run the tutorial:

<img src="./data-raw/images/run_tutorial_pane_discovr.png" width="700">

Alternatively, to run a particular tutorial from the console execute:

```
library(discovr)
learnr::run_tutorial("name_of_tutorial", package = "discovr")
```

and replace "name of tutorial" with the name of the tutorial you want to run. For example, to run tutorial 2 execute:

```
learnr::run_tutorial("discovr_02", package = "discovr")
```

The name of each tutorial is in bold in the list above. Once the command to run the tutorial is executed it will spring to life in a web browser.

### Suggested workflow

The tutorials are self-contained (you practice code in code boxes) so you don't need to use <img src="./data-raw/images/rstudio_logo.png" width="48"> at the same time. However, to get the most from them I would recommend that you create an <img src="./data-raw/images/rstudio_logo.png" width="48"> project and within that open (and save) a new RMarkdown file each time to work through a tutorial. Within that Markdown file, replicate parts of the code from the tutorial (in code chunks) and use Markdown to write notes about what you have done, and to reflect on things that you have struggled with, or note useful tips to help you remember things. Basically, write a learning journal. This workflow has the advantage of not just teaching you the code that you need to do certain things, but also provides practice in using <img src="./data-raw/images/rstudio_logo.png" width="48"> itself.

## Datasets

See the book or data descriptions for more details. This is a list of available datasets within the package. Raw CSV files are available from the book's website.

* **acdc**: Data about whether Bon Scott or Brian Johnson is the best singer of AC/DC. For details execute `?acdc`.
* **album_sales**: Ficticious data about predicting album sales from advertising, airplay and the band's image. For details execute `?album_sales`.
* **animal_bride**: Ficticious data about life satisfaction when married to a dog or a goat. For details execute `?animal_bride`.
* **beckham_1929**: Data from a study by Beckham (1929). For details execute `?beckham_1929`.
* **big_hairy_spider**: Ficticious data about whether anxiety is greater after exposure to real spiders or pictures of spiders. For details execute `?big_hairy_spider`.
* **biggest_liar**: Ficticious data about creativity and telling lies. For details execute `?biggest_liar`.
* **bronstein_2019**: Data about whether delusion proneness predicts belief in fake news because of less analytic thinking. For details execute `?bronstein_2019`.
* **bronstein_miss_2019**: The data in [bronstein_2019] but with missing values inserted using MCAR amputation. For details execute `?bronstein_miss_2019`.
* **catterplot**: Ficticious data for plotting a catterplot. For details execute `?catterplot`.
* **cat_dance**: Ficticious data about training cats to dance. For details execute `?cat_dance`.
* **cat_reg**: Ficticious data about training cats to dance. For details execute `?cat_reg`.
* **chamorro_premuzic**: Data about what students want (personality wise) from their lecturers. For details execute `?chamorro_premuzic`.
* **child_aggression**: Ficticious data (based on real research) about predicting aggression in children. For details execute `?child_aggression`.
* **coldwell_2006**: Data predicting childhood adjustment from various parenting variables. For details execute `?coldwell_2006`.
* **daniels_2012**: Data about the effects of sexualised sports images on self-image. For details execute `?daniels_2012`.
* **dark_lord**: Ficticious data about the subliminal messages in songs. For details execute `?dark_lord`.
* **download**: Ficticious data about the download music festival and being smelly. For details execute `?download`.
* **df_beta**: Ficticious data used to illustrate the DF Beta statistic. For details execute `?df_beta`.
* **essay_marks**: Ficticious data about essay marking. For details execute `?essay_marks`.
* **exam_anxiety**: Ficticious data about exam performance, anxiety and revision. For details execute `?exam_anxiety`.
* **gelman_2009**: Data used to critically evaluate the explanations (and claim) that there are more beautiful women than men in the world. For details execute `?gelman_2009`.
* **glastonbury**: More ficticious data about music festivals and being smelly. For details execute `?glastonbury`.
* **grades**: Ficticious data about statistics grades. For details execute `?grades`.
* **ice_bucket**: Data about the ice bucket challenge. For details execute `?ice_bucket`.
* **invisibility_cloak**: Ficticious data about how much mischief peopel would get up to if they had an invisibility cloak. For details execute `?invisibility`.
* **invisibility_rm**: Ficticious data about how much mischief peopel would get up to if they had an invisibility cloak but using a repeated measures design. For details execute `?invisibility_rm`.
* **hiccups**: Ficticious data on digital rectal stimulation and hiccups. For details execute `?hiccups`.
* **honesty_lab**: Ficticious data about perceptions of honesty. For details execute `?honesty_lab`.
* **jiminy_cricket**: Ficticious data about whether wishing on a star makes you successful. For details execute `?jiminy_cricket`.
* **johns_2012**: Data about whether the colour red is a mating signal to men. For details execute `?johns_2012`.
* **lambert_2012**: Data about whether pornography use is related to relationhsip commitment and infidelity. For details execute `?lambert_2012`.
* **massar_2012**: Data about whether gossiping has an evolutionary function. For details execute `?massar_2012`.
* **mcnulty_2008**: Simulated data to match the results of a study about whether attractivenes sis linked to the support given within a relationship. For details execute `?mcnulty_2008`.
* **men_dogs**: Ficticious data about whether men exhibit dog-like behaviours (compared to dogs). For details execute `?men_dogs`.
* **metal_health**: Ficticious data about whether listening to heavy metal negatively affects mental health. For details execute `?metal_health`.
* **metallica**: Data about thrash metal nband, Metallica. For details execute `?metallica`.
* **notebook**: Ficticious data about whether watching the film the notebook is emotionally arousing. For details execute `?notebook`.
* **ong_2011**: Data about social media profile pictures and personality traits. For details execute `?ong_2011`.
* **ong_tidy**: Data about social media profile pictures and personality traits. For details execute `?ong_tidy`.
* **pubs**: Data illustrating the difference between an outlier and an influencial case. For details execute `?pubs`.
* **r_exam**: Fictitious data relating to an R exam at two universities. For details execute `?r_exam`.
* **roaming_cats**: Ficticious data about how far cats roam from their homes For details execute `?roaming_cats`.
* **self_help**: Ficticious data about whether self-help books improve relationship satisfaction. For details execute `?self_help`.
* **self_help_dsur**: Ficticious data about whether self-help books improve relationship satisfaction compared to statistics books. For details execute `?self_help_dsur`.
* **social_anxiety**: Ficticious (I think) data about whether social anxiety symptoms are specific to social anxiety. For details execute `?social_anxiety`.
* **social_media**: Ficticious data about the effects of social media on grammar. For details execute `?social_media`.
* **shopping**: Ficticious data about shopping For details execute `?shopping_exercise`.
* **students**: I can't even remember what this data file contains. For details execute `?student`.
* **supermodel**: Ficticious data about supermodel salaries. For details execute `?supermodel`.
* **tablets**: Ficticious data about predicting the desirability of computing tablets. For details execute `?tablets`.
* **tea_15**: Ficticious data based on real data about cognitive functioning and drinking tea. For details execute `?tea_makes_you_brainy_15`.
* **tea_716**: Ficticious data based on real data about cognitive functioning and drinking tea. For details execute `?tea_makes_you_brainy_716`.
* **teaching**: Ficticious data about the success of different methods of treaching. For details execute `?method_of_teaching`.
* **video_games**: Ficticious data about the relationship between video game use, callous unemotional traits and aggression. For details execute `?video_games`.
* **tuk_2011**: Data about whether needing to urinate helps decision making. For details execute `?tuk_2011`.
* **zhang_sample**: Data about whether performing a maths test under a different name assists performance. For details execute `?zhang_2013_subsample`.

## Smart Alex solutions

Solutions for end of chapter tasks are available at [www.discovr.rocks](https://www.discovr.rocks/solutions/alex/).

## Labcoat Leni solutions

Solutions for the Labcoat Leni tasks are available at [www.discovr.rocks](https://www.discovr.rocks/solutions/leni/).

## Chapter code

Although I recommend working through the interactive solutions, each book Chapter has online code and a downloadable R Markdown file available from [www.discovr.rocks](https://www.discovr.rocks/solutions/code/).
