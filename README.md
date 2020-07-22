# US Job Analysis in R
[![Makes people smile](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://github.com/iamsivab)

![Hits](https://hitcounter.pythonanywhere.com/count/tag.svg?url=https%3A%2F%2Fgithub.com%2Fiamsivab%2FUS-Job-Market-Analysis)
## US Job Analysis in R
[![Generic badge](https://img.shields.io/badge/Text-Mining-teal.svg?style=for-the-badge)](https://github.com/iamsivab/US-Job-Market-Analysis) 
[![Generic badge](https://img.shields.io/badge/LinkedIn-Connect-blue.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/iamsivab/) [![Generic badge](https://img.shields.io/badge/R-Language-blue.svg?style=for-the-badge)](https://github.com/iamsivab/US-Job-Market-Analysis/) [![ForTheBadge uses-git](http://ForTheBadge.com/images/badges/uses-git.svg)](https://GitHub.com/)

#### This Project contains my Analysis of the [Data](https://download.bls.gov/pub/time.series/la/la.data.1.CurrentS") [#TimeSeries](https://github.com/iamsivab/US-Job-Market-Analysis) and applying time series prediction

[![GitHub repo size](https://img.shields.io/github/repo-size/iamsivab/US-Job-Market-Analysis.svg?logo=github&style=social)](https://github.com/iamsivab) [![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/iamsivab/US-Job-Market-Analysis.svg?logo=git&style=social)](https://github.com/iamsivab/)[![GitHub top language](https://img.shields.io/github/languages/top/iamsivab/US-Job-Market-Analysis.svg?logo=python&style=social)](https://github.com/iamsivab)

#### Few popular hashtags - 
### `#JobMarketAnalysis` `#JobSearch` `#Classification`
### `#dataanalysis` `#UnitedStates` `#datavisualization`

### Motivation
Job analysis (also known as work analysis) is a family of procedures to identify the content of a job in terms of activities involved and attributes or job requirements needed to perform the activities. Job analysis provides information of organizations which helps to determine which employees are best fit for specific jobs. Through job analysis, the analyst needs to understand what the important tasks of the job are, how they are carried out, and the necessary human qualities needed to complete the job successfully.

### About the Project

The process of job analysis involves the analyst describing the duties of the incumbent, then the nature and conditions of work, and finally some basic qualifications. After this, the job analyst has completed a form called a job psychograph, which displays the mental requirements of the job.[2] The measure of a sound job analysis is a valid task list. This list contains the functional or duty areas of a position, the related tasks, and the basic training recommendations. Subject matter experts (incumbents) and supervisors for the position being analyzed need to validate this final list in order to validate the job analysis

#### Data Preparation for Analysis

[![Made with love](https://forthebadge.com/images/badges/built-with-love.svg)](https://www.linkedin.com/in/iamsivab/) [![ForTheBadge built-with-swag](http://ForTheBadge.com/images/badges/built-with-swag.svg)](https://www.linkedin.com/in/iamsivab/)

```R
# Downloading data
ur.data<-fread("https://download.bls.gov/pub/time.series/la/la.data.1.CurrentS")

# Download series ids

ur.series<-fread("https://download.bls.gov/pub/time.series/la/la.series")

# subset data
ur.list<-ur.series[area_type_code =="A" &   #get states
                     measure_code == "3"  &   #get unemployment rate
                     seasonal == "S",         #get seasonally adjusted data
                   c("series_id","area_code","series_title"),
                   with=F]

## Get state names and area crosswalk
ur.area<-fread("https://download.bls.gov/pub/time.series/la/la.area",
               col.names=
                 c("area_type_code","area_code","area_text","display_level",
                   "selectable","sort_sequence"))                   

# merge data
ur.dt<-merge(ur.data,ur.list,by="series_id",all.y=T)
```

A job search currently gives in download.bls.gov results and provides lots of interesting information that we would like to capture.
#### Explanation
Job analysis aims to answer questions such as:

`Why does the job exist?`
`What physical and mental activities does the worker undertake?`
`When is the job to be performed?`
`Where is the job to be performed?`
`Under What conditions it is to be performed?`

### Libraries Used

```R
library(data.table)
library(quantmod)
library(tidyverse)
library(tweenr)
library(animation)
library(ggplot2)
library(ggthemes)
install.packages("artyfarty")
library(artyfarty)
library(extrafont)
```

![R Studio](https://img.shields.io/badge/R-data.table-blue.svg?style=flat&logo=r&logoColor=white) 
![R Studio](https://img.shields.io/badge/R-quantmod-blue.svg?style=flat&logo=r&logoColor=white)
![R Studio](https://img.shields.io/badge/R-tidyverse-blue.svg?style=flat&logo=r&logoColor=white) 
![R Studio](https://img.shields.io/badge/R-animation-blue.svg?style=flat&logo=r&logoColor=white) 
![R Studio](https://img.shields.io/badge/R-tweenr-blue.svg?style=flat&logo=r&logoColor=white)
![R Studio](https://img.shields.io/badge/R-ggplot2-blue.svg?style=flat&logo=r&logoColor=white) 
![R Studio](https://img.shields.io/badge/R-ggthemes-blue.svg?style=flat&logo=r&logoColor=white) 
![R Studio](https://img.shields.io/badge/R-artyfarty-blue.svg?style=flat&logo=r&logoColor=white) 
![R Studio](https://img.shields.io/badge/R-extrafont-blue.svg?style=flat&logo=r&logoColor=white) 

### Installation

- Install **quantmod** using pip command: `install.packages("quantmod")`
- Install **tidyverse** using pip command: `install.packages("tidyverse")`
- Install **tweenr** using pip command: `install.packages("tweenr")`
- Install **animation** using pip command: `install.packages("animation")`
- Install **ggplot2** using pip command: `install.packages("ggplot2")`
- Install **ggthemes** using pip command: `install.packages("ggthemes")`
- Install **artyfarty** using pip command: `install.packages("artyfarty")`
- Install **extrafont** using pip command: `install.packages("extrafont")`

### How to run?

[![R Studio](https://img.shields.io/badge/R-us_sales.R.-lightgrey.svg?logo=R&style=social)](https://github.com/iamsivab/US-Job-Market-Analysis/blob/master/US%20Sales.R)


### Project Reports

[![report](https://img.shields.io/static/v1.svg?label=Project&message=Report&logo=microsoft-word&style=social)](https://github.com/iamsivab/US-Job-Market-Analysis/)

- [Download](https://github.com/iamsivab/US-Job-Market-Analysis/) for the report.

### Useful Links

1. [Python vs R: How to Analyse 4000 Job Advertisements Using Shiny & Machine Learning](https://towardsdatascience.com/python-vs-r-what-i-learned-from-4-000-job-advertisements-ab41661b7f28)
 
### Related Work

[![Sentiment Analysis](https://img.shields.io/static/v1.svg?label=Text&message=Mining&color=lightgray&logo=linkedin&style=social&colorA=critical)](https://www.linkedin.com/in/iamsivab/) [![GitHub top language](https://img.shields.io/github/languages/top/iamsivab/US-Job-Market-Analysis.svg?logo=php&style=social)](https://github.com/iamsivab/)

[Text Mining Analyzer](https://github.com/iamsivab/Text-Mining-in-R) - A Detailed Report on the Analysis


### Contributing

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?logo=github)](https://github.com/iamsivab/US-Job-Market-Analysis/pulls) [![GitHub issues](https://img.shields.io/github/issues/iamsivab/US-Job-Market-Analysis?logo=github)](https://github.com/iamsivab/US-Job-Market-Analysis/issues) ![GitHub pull requests](https://img.shields.io/github/issues-pr/viamsivab/US-Job-Market-Analysis?color=blue&logo=github) 
[![GitHub commit activity](https://img.shields.io/github/commit-activity/y/iamsivab/US-Job-Market-Analysis?logo=github)](https://github.com/iamsivab/US-Job-Market-Analysis/)

- Clone [this](https://github.com/iamsivab/US-Job-Market-Analysis/) repository: 

```bash
git clone https://github.com/iamsivab/US-Job-Market-Analysis.git
```

- Check out any issue from [here](https://github.com/iamsivab/US-Job-Market-Analysis/issues).

- Make changes and send [Pull Request](https://github.com/iamsivab/US-Job-Market-Analysis/pull).
 
### Need help?

[![Facebook](https://img.shields.io/static/v1.svg?label=follow&message=@iamsivab&color=9cf&logo=facebook&style=flat&logoColor=white&colorA=informational)](https://www.facebook.com/iamsivab)  [![Instagram](https://img.shields.io/static/v1.svg?label=follow&message=@iamsivab&color=grey&logo=instagram&style=flat&logoColor=white&colorA=critical)](https://www.instagram.com/iamsivab/) [![LinkedIn](https://img.shields.io/static/v1.svg?label=connect&message=@iamsivab&color=success&logo=linkedin&style=flat&logoColor=white&colorA=blue)](https://www.linkedin.com/in/iamsivab/)

:email: Feel free to contact me @ [balasiva001@gmail.com](https://mail.google.com/mail/)

[![GMAIL](https://img.shields.io/static/v1.svg?label=send&message=balasiva001@gmail.com&color=red&logo=gmail&style=social)](https://www.github.com/iamsivab) [![Twitter Follow](https://img.shields.io/twitter/follow/iamsivab?style=social)](https://twitter.com/iamsivab)


### License

MIT &copy; [Sivasubramanian](https://github.com/iamsivab/US-Job-Market-Analysis/blob/master/LICENSE)

[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/0)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/0)[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/1)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/1)[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/2)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/2)[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/3)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/3)[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/4)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/4)[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/5)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/5)[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/6)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/6)[![](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/images/7)](https://sourcerer.io/fame/iamsivab/iamsivab/US-Job-Market-Analysis/links/7)


[![GitHub license](https://img.shields.io/github/license/iamsivab/US-Job-Market-Analysis.svg?style=social&logo=github)](https://github.com/iamsivab/US-Job-Market-Analysis/blob/master/LICENSE) 
[![GitHub forks](https://img.shields.io/github/forks/iamsivab/US-Job-Market-Analysis.svg?style=social)](https://github.com/iamsivab/US-Job-Market-Analysis/network) [![GitHub stars](https://img.shields.io/github/stars/iamsivab/US-Job-Market-Analysis.svg?style=social)](https://github.com/iamsivab/US-Job-Market-Analysis/stargazers) [![GitHub followers](https://img.shields.io/github/followers/iamsivab.svg?label=Follow&style=social)](https://github.com/iamsivab/)
