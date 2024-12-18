# The Kids Are All Right: Investigating the Susceptibility of Teens and Adults to YouTube Giveaway Scams

This repository contains the survey instrument, analysis scripts, and de-identified data for the NDSS '25 paper "The Kids Are All Right: Investigating the Susceptibility of Teens and Adults to YouTube Giveaway Scams" by Elijah Bouma-Sims, Lily Klucinec, Mandy Lanyon, Lorrie Faith Cranor, Julie Downs. This paper has been accepted to [NDSS 2025](https://www.ndss-symposium.org/ndss2025/). When avliable, the paper will be accessible from [https://dx.doi.org/10.14722/ndss.2025.240342](https://dx.doi.org/10.14722/ndss.2025.240342).


## Requirements
Analysis was performed using R version 4.3.3, however, it is not expected that the version of R will effect the results. The analysis script is distributed in the form of an R Markdown (.rmd) file, requiring [RStudio](https://posit.co/download/rstudio-desktop/) to view.  Data is stored in Excel format (.xlsx), which requires Microsoft Excel or compatible spreadsheet software to view. The survey is in Microsoft Word format (.docx), which requires Microsoft Word or compatible document editing software to view. Media is distributed as PNG files for images and MP4 files for videos. Finally, the following readily available R packages are used in the analysis script: "RVAideMemoire",  "dplyr", "rstatix", "readxl", "rcompanion", "DescTools", and "stringr." 

## File structure
* ```data\``` contains the data obtained from the experiment and metadata explaining the meaning of each field.
  * ```data\df_analysis.xlsx``` contains participant's responses.
  * ```data\dictionary.xlsx``` lists the name of each field in ```data\df_analysis.xlsx``` alongside a descriptor of the field. References to question numbers in ```data\dictionary.xlsx``` refer to the adult survey (```survey\experiment\adult_survey.docx```) unless otherwise specified.
  * ```data\codebook.xlsx``` contains defintions of the codes used to describe qualitative data. 
* ```analysis.rmd``` contains the analysis code that was used to produce results for the paper. To run this script on none Windows systems, you will need to change the data path (set in the variable ```data_path```) to the apporpriate format.
  * ```analysis.html``` is the compiled form of this R markdown file.
* ```media\``` contains the videos and images presented to partiicpants in the experiment.
  * ```media\search_results\``` contains the search result images.
  * ```media\yt_videos\``` contains the redacted YouTube videos.
  * ```media\web_videos\``` contains the videos of a user scrolling through the webistes. The videos and search results are labeled based on the categorical labels described in ```data\dictionary.xlsx``` under ```scam_condition```, ```legit_condition```, ```spotify_tn_selection```, and ```roblox_tn_selection```. ```media\audio_check.mp4``` is the video used to verify that partiicpants could hear audio/read captions during the consent process.
* ```survey\``` contains the text of all of the survey instruments userd in our study.  
  * ```survey\consent\``` contains the informed consent forms provided to participants.
    * ```survey\consent\adult_consent.docx``` is the informed consent form presented to Prolific crowdworkers.
    * ```survey\consent\parental_consent.docx``` is the informed consent form presented to parents of teenage partiicpants.
    * ```survey\consent\ES_parental_consent.docx``` is the Spanish translated version of the parental consent form.
    * ```survey\consent\teen_assent.docx``` is the assent form presented to teenage participants.  
  * ```survey\experiment\``` contains the text of the survey instruments used to collect data for the experiment.
    * ```survey\experiment\parent_survey.docx``` is the demographic questionaire which parents filled out on behalf of their children.
    * ```survey\experiment\ES_parent_survey.docx``` is the Spanish translated version of the parental demographic questionaire.
    * ```survey\experiment\teen_survey.docx``` contains the survey instrument which teenage participants saw.
    * ```survey\experiment\adult_survey.docx``` contains the survey instrument whch adult partiicpants saw.
    * ```survey\experiment\teen_compensation_survey.docx``` contains the survey used to collect email addresses from teen participants for compensation purposes.
* ```recruitment\``` contains the recruitment materials used for the experiment.
  * ```recruitment\paremt_poster.png``` is the poster distributed to parents via snowball sampling and Peachjar.
  * ```recruitment\prolific.docx``` contains the text of the posting used to recruit crowdworkers on Prolific.
