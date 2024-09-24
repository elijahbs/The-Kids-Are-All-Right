# The Kids Are All Right: Investigating the Susceptibility of Teens and Adults to YouTube Giveaway Scams

This repository contains the survey instrument, analysis scripts, and de-identified data for the NDSS '25 paper "The Kids Are All Right: Investigating the Susceptibility of Teens and Adults to YouTube Giveaway Scams" by Elijah Bouma-Sims, Lily Klucinec, Mandy Lanyon, Lorrie Faith Cranor, Julie Downs.

## Requirements
Analysis was performed using R version 4.3.3, however, it is not expected that the version of R would effect the results. The analysis script is distributed in the form of an R Markdown (.rmd) file, requiring [RStudio](https://posit.co/download/rstudio-desktop/) to view.  Data is stored in Excel format (.xlsx), which requires Microsoft Excel or compatible spreadsheet software to view. The survey is in Microsoft Word format (.docx), which requires Microsoft Word or compatible document editing software to view. Finally, the following readily available R packages are used in the analysis script: "dplyr", "rstatix", "readxl", "rcompanion", "DescTools",, and "stringr." 

## File structure
* ```data\``` contains the data obtained from the experiment and metadata explaining the meaning of each field. ```data\df_analysis.xlsx``` contains participant's responses. ```data\dictionary.xlsx``` lists the name of each field in ```df_analysis.xlsx``` alongside a descriptor of the field.
* ```data\qualitative_coding\``` contains N excel files with the qualitative codes assigned for partiicpants' responses. For example, ```legit_exp.xlsx``` lists the codes for the explanations in response to viewing the legitimate YouTube video.
* ```media\``` contains the videos and images presented to partiicpants in the experiment. ```media\search_results\``` contains the search result images, ```media\yt_videos\``` contains the redacted YouTube videos, and ```media\web_videos\``` contains the videos of a user scrolling through the webistes. The videos and search results are labeled based on the categorical labels described in ```data\dictionary.xlsx```
* ```survey.docx``` contains the text of the survey instrument

