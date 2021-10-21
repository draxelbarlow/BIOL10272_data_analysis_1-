---
title       : "Data Analysis 1"
subtitle    : "BIOL10272: Practical Techniques"
author      : Dr Axel Barlow
job         : "email: axel.barlow@ntu.ac.uk"
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : zenburn      # {zenburn, tomorrow, solarized-dark, ...}
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {selfcontained, standalone, draft}
knit        : slidify::knit2slides
logo        : ntu-shield.png
biglogo     : NTU_open-graph.png
assets      : {assets: ../../assets}
license     : by-nc-sa
github:
  user: draxelbarlow
  repo: BIOL10272_data_analysis_1
  branch: "gh-pages"
---



<!-- adding bold and italic options -->
<style>
em {
  font-style: italic
}
strong {
  font-weight: bold;
}
</style>

## Data analysis 1

  - Organisation
  - Why is data analysis important?
  - Computers and data analysis
  - Variables
  - Collecting data
  - Organising data in a table

--- .segue .dark 

## Organisation

--- &vcenter

## What will you learn?

<img src="assets/fig/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" width="100%" height="100%" style="display: block; margin: auto;" />

--- .class #id

## Organisation

- 4 online lectures
- Seminar 1: `Excel` and `R`. Online with optional drop in
- Seminar 2: `R`. Online with optional drop in
- Revision session
  
<img src="./assets/img/learn_wide.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="100%" />

--- .class #id

## How do you access software?

- Software: `Excel` and `R` running through `Rstudio`
- NTU supported Virtual Machines
- All you need is a computer, internet connection and a web browser (e.g. `Chrome`, `FireFox`)
- At home or on campus
- Full instructions later

<img src="./assets/img/code_wide.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" width="100%" />

--- .class #id

## Where can you find additional information?

- Discussion boards on `NOW` (post anonymously)
- Web resources e.g. www.khanacademy.org
- Library: www.ntu.ac.uk/m/library
- General statistics: *Data Analysis and Statistics with* `R`. https://dzchilds.github.io/stats-for-bio/
- More advanced bioinformatics: `R` *for Data Science*. https://r4ds.had.co.nz/

<img src="./assets/img/adult_learning.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="100%" />

--- .segue .dark 

## Why is data analysis important?

--- .class #id

## The human mind works statistically

<q> The brain produces feelings of confidence that inform decisions the same way statistics pulls patterns out of noisy data </q>

Cold Spring Harbor Laboratory. ScienceDaily, 4 May 2016.

--- .class #id

## Supermarket X is cheaper than supermarket Y

<img src="./assets/img/supermarket.png" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" width="100%" />

--- &twocol

## Lab work also requires data analysis

*** =left

- Quantitative PCR
- Quantify gene expression
- Or viral load

<img src="./assets/img/Qpcr-cycling.png" title="plotting example" alt="plotting example" width="100%" />
*Zuzanna K. Filutowska, CC BY-SA 3.0*

*** =right

<img src="./assets/img/pipette.JPG" title="plot of chunk unnamed-chunk-7" alt="plot of chunk unnamed-chunk-7" width="70%" style="display: block; margin: auto;" />

--- .class #id

## Phosphate Assay lab

<img src="./assets/img/Screenshot from 2021-10-21 11-47-59.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="95%" style="display: block; margin: auto;" />

--- .class #id

## Also a tool for science communication

<q>France seeing exponential rise...</q>

<q>Flattening the Coronavirus curve...</q>

<q>R number is now between 1.1 and 1.4...</q>

--- .class bg:white

## Also a tool for science communication

<iframe src = 'https://coronavirus.data.gov.uk/' height='600px'></iframe>

--- .segue .dark 

## Computers and data analysis

--- .class #id

## In school/college, you may have used these

<img src="./assets/img/calculator-2391810.jpg" title="plot of chunk unnamed-chunk-9" alt="plot of chunk unnamed-chunk-9" width="80%" style="display: block; margin: auto;" />

--- .class #id

## Modern science relies on computers

<img src="./assets/img/thinkpad-computer-1155173.png" title="plot of chunk unnamed-chunk-10" alt="plot of chunk unnamed-chunk-10" width="70%" style="display: block; margin: auto;" />

--- .class #id

## Bioinformatics and data science

- Biology + informatics
- Computational analysis of biological data
- A key part of modern biological research
- Links biology, computer science, mathematics and statistics
- Part of the emerging field of data science

<img src="./assets/img/datascience_sexy.png" title="plot of chunk unnamed-chunk-11" alt="plot of chunk unnamed-chunk-11" width="70%" />

*Harvard Business Review*

--- &twocol

## Case study: Genomics

*** =left

**The human genome**

- DNA comprising pairs of nucleotide bases
- 3,600,000,000 total base-pairs
- 3.6 Gigabases
- 2 copies per cell
- ~2 metres of DNA

**This represents**

- 1,028,571 pages of text
- 80 boxes of copier paper
- 1,096 years of typing

*** =right

<img src="./assets/img/Dna-base-flipping.svg" title="plot of chunk unnamed-chunk-12" alt="plot of chunk unnamed-chunk-12" width="100%" />

*Magladem96, CC BY-SA 3.0*

--- &twocol

## Case study: Genomics

*** =left

**This Illumina NovaSeq 6000 produces:**
- 40 billion DNA sequences (20,000,000,000)
- each 150 bp in length
- 6,000 Gigabases of data
- equivalent to ~1,600 human genomes
- in < 2 days

*** =right

<img src="./assets/img/NovaSeq_6000.jpg" title="plot of chunk unnamed-chunk-13" alt="plot of chunk unnamed-chunk-13" width="70%" />

*Magnus Manske, CC BY-SA 4.0*

--- &twocol

## Bioinformatics means you can play with cool kit

*** =left

<img src="./assets/img/apple-1282241.jpg" title="plot of chunk unnamed-chunk-14" alt="plot of chunk unnamed-chunk-14" width="100%" style="display: block; margin: auto;" />

**Laptop**

- 6 CPUs
- 16 Gb RAM
- 0.5 Tb Disc space

*** =right

<img src="./assets/img/hamilton.png" title="plot of chunk unnamed-chunk-15" alt="plot of chunk unnamed-chunk-15" width="100%" />

**Hamilton**

- 512 CPUs
- 4 Tb RAM (4,000 Gb)
- 67 Tb Disc space

--- &twocol

## Software: `Microsoft Excel`

*** =left

- Spreadsheet based program
- Widely used across many professions
- Grid of **cells**
- Arranged in **rows** and **columns**
- Cells can contain **data** or **functions**
- Can produce graphs
- Can perform various statistical tests and analyses
- Proprietary software
- Max 1,048,576 rows by 16,384 columns
- Max 2Gb file size

*** =right

<img src="./assets/img/Microsoft_Office_Excel_(2018–present).svg" title="plot of chunk unnamed-chunk-16" alt="plot of chunk unnamed-chunk-16" width="40%" style="display: block; margin: auto;" />

<img src="./assets/img/Microsoft_Excel.png" title="plot of chunk unnamed-chunk-17" alt="plot of chunk unnamed-chunk-17" width="100%" />

*Used with permission from* `Microsoft`.

--- &twocol

## Software: `R`

*** =left

- **Programming language**
- Executed through the **command line**
- Or `Rstudio` environment
- Fully **open source**
- Many add-on **packages**
- Can handle very large files
- Vast range of analyses
- High quality graphs and diagrams
- Websites
- Reports
- This presentation!


*** =right

<img src="./assets/img/R_logo.svg.png" title="plot of chunk unnamed-chunk-18" alt="plot of chunk unnamed-chunk-18" width="30%" style="display: block; margin: auto;" />

*CC-BY-SA 4.0*

<img src="./assets/img/Rstudio.png" title="plot of chunk unnamed-chunk-19" alt="plot of chunk unnamed-chunk-19" width="100%" />

*PAC2, AGPL*


--- .class bg:white

## Try doing this in `Excel` ;)

<img src="assets/fig/unnamed-chunk-20-1.gif" title="plot of chunk unnamed-chunk-20" alt="plot of chunk unnamed-chunk-20" width="95%" height="95%" style="display: block; margin: auto;" />

--- .segue .dark 

## Variables

--- .class #id bg:white

## Science finds things that affect other things

<img src="./assets/img/doctor-5342890.jpg" title="plot of chunk unnamed-chunk-21" alt="plot of chunk unnamed-chunk-21" width="80%" style="display: block; margin: auto;" />

--- .class #id bg:white

## Science finds things that affect other things

<img src="./assets/img/agar-60571.jpg" title="plot of chunk unnamed-chunk-22" alt="plot of chunk unnamed-chunk-22" width="85%" style="display: block; margin: auto;" />

--- .class #id bg:white

## Science finds things that affect other things

<img src="./assets/img/red-eye-frog-2815683.png" title="plot of chunk unnamed-chunk-23" alt="plot of chunk unnamed-chunk-23" width="90%" />

--- .class #id 

## These things are called variables

### A variable is something that can be measured or counted

**There are three main types:**

1. Categorical variables

2. Ordinal variables

3. Quantitative variables
  - Continuous
  - Discrete

### The type of variable determines how data should be analysed and visualised

--- .class #id 

## Categorical variables

*[Can be referred to as qualitative or nominal variables]*

  >- Things that have distinct categories
  >- Qualitative (assigned or named, not quantified)
  >- A fixed (or limited) number of possibilities
  >- Categories cannot be divided or multiplied
  >- Examples: 
    + Presence/absence of anything
    + DNA nucleotides
    + species

--- .class #id 

## Ordinal variables

*[Can be referred to as ranked variables]*

  >- Things that can be ranked
  >- Categories that can be put in a sequence
  >- Qualitative (assigned or named, not quantified)
  >- A fixed (or limited) number of possibilities
  >- Categories cannot be divided or multiplied
  >- But we can identify a middle value
  >- Examples: 
    + Often used in questionnaires, e.g. dislike, indifferent, like
    + Degrees: BSc, MSc, PhD

--- .class #id 

## Quantitative variables

*[Can be referred to as numeric, interval or ratio variables]*

  >- Things that can be measured numerically
  >- Typically have **units**
  >- Values can be divided or multiplied
  >- **Continuous**
    + An infinite number of possibilities
    + Accuracy only limited by the experimental method
    + Temperature, distance, speed, time
  >- **Discrete**
    + Numerical measurements where only certain values are possible
    + Counts, e.g. number of patients, molecules, etc.

--- .segue .dark 

## Collecting data

--- .class #id 

## Collecting data

### A variable is something that can be measured or counted

- Taking a measurement or count is an **observation**
- The information you collect is a **value** (or datum)
- All the values together are your **data**
- The number of observations is your **sample size** (often expressed as `N`)

### Sometimes you record multiple variables from the same thing
  - *Patient number = 1234, gender = M, age = 24, heart rate = 70 bpm*
  - Here we have data for 4 variables, but it is a **single observation**

--- .class #id 

## Observations should be independent

- One observation does not affect the other
- Lack of independence can cause the sample size to be misjudged
- This is called **pseudoreplication**

>- *You measure the blood pressure of a single person 100 times*
  - 100 measurements, sample size `N` = 1 person

>- *You measure the length of 100 leaves from the same tree*
  - 100 leaves, sample size `N` = 1 tree
  
>- Note before/after measurements are fine, but these pairs represent a single observation
>- *Patient blood pressure before & after drug treatment*
  - 2 blood pressure values, sample size `N` = 1 patient

--- .class #id 

## Samples should be collected at random

- We should not bias our observations towards particular categories or values
- Often one of the most difficult aspects of study design!
- Sometimes unavoidable, requiring careful analysis and interpretation

>- *You count the number of bird species in a woodland habitat and in a lake habitat*
  - Woodland birds are harder to see

>- *You work at an diabetes clinic. You investigate how many patients smoked prior to developing diabetes*
  - You work at an diabetes clinic: all your patients develop diabetes (some of whom happen to have smoked)

--- .segue .dark 

## Organising data in a table

--- .class #id 

## Tables

### Tables are an excellent way to organise, store and analyse our data
- The format is flexible, but generally:
  + Each **row** is an observation
  + Each **column** is a variable
  + The **top row** is the variable names

>- Tables can be created and saved in `Excel`, where further analysis can be carried out
>- Bioinformaticians tend to use plain text (space, comma or tab delimited)
>- This is an ideal data format for importing into `R`

--- .class #id 

## Example tables

### Beaver body temperature


| day| time|  temp|
|---:|----:|-----:|
| 346|  840| 36.33|
| 346|  850| 36.34|
| 346|  900| 36.35|
| 346|  910| 36.42|
| 346|  920| 36.55|
| 346|  930| 36.69|
| 346|  940| 36.71|
| 346|  950| 36.75|
| 346| 1000| 36.81|
| 346| 1010| 36.88|
| 346| 1020| 36.89|

--- .class #id 

## Example tables

### Beaver body temperature: plain text


```
##    day time  temp
## 1  346  840 36.33
## 2  346  850 36.34
## 3  346  900 36.35
## 4  346  910 36.42
## 5  346  920 36.55
## 6  346  930 36.69
## 7  346  940 36.71
## 8  346  950 36.75
## 9  346 1000 36.81
## 10 346 1010 36.88
## 11 346 1020 36.89
```

--- .class #id 

## Data analysis 1

  - Organisation
  - Why is data analysis important?
  - Computers and data analysis
  - Variables
  - Collecting data
  - Organising data in a table

--- &thankyou

## Next time

**Barcharts, histograms, averages, and variability**
