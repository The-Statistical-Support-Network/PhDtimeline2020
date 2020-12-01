# PhDtimeline2020

https://davan690.github.io/PhDtimeline2020/ Submitting and managing future PhD timelines can be hard at the best of times due to unpredictable outcomes of data and analysis of results. This is made even more challenging under COVID19 conditions because of the unpredictable nature of the disease and the impacts of this both economically and socially throughout the community. See the website here: https://davan690.github.io/

A simple proposal and clean repository for my PhD planning and funding documentation using new open science methods (RMarkdown).

###### To do (NOTES)

- [ ] `DiagrammR` example of mermaid Sequence Diagrams
- [x] Integrate `dataspice` to methods
- [ ] Integrate  `tidyverse` to methods
- [ ] Integrate  `bookdown` to methods
- [ ] Integrate `tidypipes` to methods
- [ ] Gmail import scripts
- [ ] Put R code in functions
- [ ] host Planning repo on website
- [ ] Clean up landing site
- [ ] Incorporating the information Barbara passed on
- [ ] Computational reproducibility has not been achieved here yet but I hope that with some additional funding this will be possible.



##### RCode

```{r eval = T}
library(DiagrammeR)

# mermaid("
# sequenceDiagram
#   customer->>ticket seller: ask ticket
#   ticket seller->>database: seats
#   alt tickets available
#     database->>ticket seller: ok
#     ticket seller->>customer: confirm
#     customer->>ticket seller: ok
#     ticket seller->>database: book a seat
#     ticket seller->>printer: print ticket
#   else sold out
#     database->>ticket seller: none left
#     ticket seller->>customer: sorry
#   end
# ")

library(knitr)

knitr::include_graphics(path = "./img/tidyPipesDiagram.jpg")
```

Project is situated around the concept of `tidyPipes`. With this approach there are three key sections:

1. Data capture
2. Visualisation

2. Communication



##### Setup

Looking at the overall repository structure of this project helps to find the files that are driving the output of this work into a word, pdf or html document using knitr.


```
📦PhDplanning2020
 ┣ 📂.git   {THIS IS THE VERSION HISTORY USING GIT}
 ┣ 📂.Rproj.user 	{USER DATA FOR R; AUTOMATICALLY generated for each machine}
 ┣ 📂data    {SEE DETAILS BELOW}
 ┣ 📂docs     {THIS IS THE OUTWARD FACING DATA AND FILES HOSTED ON gitHUB}
 ┣ 📂img
 ┃ ┣ 📜art_piece1.jpg
 ┃ ┣ 📜draftTimeline.png
 ┃ ┣ 📜image-20200811120856219.png
 ┃ ┣ 📜image-20200811121400686.png
 ┃ ┗ 📜phdStructure.jpg
 ┣ 📂imgs
 ┃ ┣ 📜art_piece1.jpg
 ┃ ┣ 📜calanthony.png
 ┃ ┣ 📜phdStructure.jpg
 ┃ ┗ 📜tidyPipesDiagram.jpg
 ┣ 📂inst
 ┃ ┗ 📂rmarkdown
 ┃ ┃ ┗ 📂templates
 ┃ ┃ ┃ ┗ 📂template-name
 ┃ ┃ ┃ ┃ ┣ 📂skeleton
 ┃ ┃ ┃ ┃ ┃ ┗ 📜skeleton.Rmd
 ┃ ┃ ┃ ┃ ┗ 📜template.yaml
 ┣ 📂R
 ┃ ┣ 📂demo_scripts
 ┃ ┃ ┣ 📜calandarDemo.R
 ┃ ┃ ┗ 📜timeExamples.R
 ┃ ┣ 📂old_scripts
 ┃ ┃ ┗ 📜chapter_timelineOLD.R
 ┃ ┣ 📜berndsKEYdatesOUTPUT.R
 ┃ ┣ 📜berndsphdcalendar.R
 ┃ ┣ 📜chapteONLYr_timeline.R
 ┃ ┣ 📜chapter_timelineALL.R
 ┃ ┣ 📜dataWranglingScript.R
 ┃ ┣ 📜importScript.R
 ┃ ┣ 📜milestonesALL.R
 ┃ ┗ 📜phdcalendar.r
 ┣ 📂vignettes			{These are short demos or scripts that use this data}
 ┃ ┣ 📜01-timeline.Rmd
 ┃ ┣ 📜02-calendar.Rmd
 ┃ ┣ 📜03-tasklist.Rmd
 ┃ ┣ 📜04-application.Rmd
 ┃ ┣ 📜05-summary.Rmd
 ┃ ┣ 📜06-references.Rmd
 ┃ ┣ 📜Calendar.Rmd
 ┃ ┣ 📜Calendar2.Rmd
 ┃ ┣ 📜CasualWork.Rmd
 ┃ ┣ 📜Covid19.Rmd
 ┃ ┣ 📜DataWrangling.Rmd
 ┃ ┣ 📜image-20200811120856219.png
 ┃ ┣ 📜image-20200811121400686.png
 ┃ ┣ 📜README.Rmd
 ┃ ┣ 📜reportTemplate.Rmd
 ┃ ┣ 📜Timeline.Rmd
 ┃ ┗ 📜VarianceEstimationOfSSMModels.Rmd
 ┣ 📂_book
 ┣ 📂_bookdown_files
 ┣ 📜.gitignore
 ┣ 📜.Rhistory
 ┣ 📜banner.html
 ┣ 📜book.bib
 ┣ 📜index.Rmd
 ┣ 📜LICENSE
 ┣ 📜ms2.docx
 ┣ 📜ms3.docx
 ┣ 📜now.json
 ┣ 📜PhDplanningAUG2020.Rproj
 ┣ 📜PhDtimeline2020.docx
 ┣ 📜preamble.tex
 ┣ 📜style.css
 ┣ 📜toc.css
 ┣ 📜VarianceEstimationOfSSMModels.Rmd
 ┣ 📜_bookdown.yml
 ┣ 📜_main.log
 ┣ 📜_main.Rmd
 ┗ 📜_output.yml
```
