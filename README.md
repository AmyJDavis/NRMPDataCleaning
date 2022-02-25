
# Guide to use NRMP Data Cleaning Shiny App

Below is a step by step guide on how to open and use the NRMP Data Cleaning App. The App can be accessed by link, or by running the program through R. 

## Direct link to App

 https://ajdavis.shinyapps.io/mis_datacheck_publish/  
 - The link above takes you directly to the app and works as a normal webpage. This is a reasonable option for access. However, there is a threshold on how many users can utilize the app through the link and may be slower. The faster and more stable way to access the app is by running it through R (described below). 

## Files included

The following files need to be added to a folder that will serve as a working directory  
1.	DataCheckingErrors.xls  
2.	DataCheckingErrors.pdf (needs to be in a folder titled "www" and that folder needs to be in your working directory)
3.	USDA_bw_transparent.png (needs to be in a folder titled "www" and that folder needs to be in your working directory)

The following file is your raw code to copy and paste into R to run the shiny app (used in Step 4)  
1.	app.R

## Step by Step to Launch App From R

### Step 1: Download R and RStudio (if already downloaded proceed to Step 2)

- Submit an IT ticket requesting to have R and R Studio (latest versions) installed 

#### -OR-

- If you have administrative privileges on your computer, do either of the following:  

###### Windows Users - to install R
  
   1. Open an internet browser and go to www.r-project.org. 
   2. Click the "download R" link in the middle of the page under "Getting Started." 
   3. Select a CRAN location (a mirror site) and click the corresponding link. 
   4. Click on the "Download R for Windows" link at the top of the page. 
   5. Click on the "install R for the first time" link at the top of the page. 
   6. Click "Download R for Windows" and save the executable file somewhere on your computer.  Run the .exe file and follow the installation instructions. 
   
##### Mac Users - to install R
    
   1. Open an internet browser and go to www.r-project.org.
   2. Click the "download R" link in the middle of the page under "Getting Started."
   3. Select a CRAN location (a mirror site) and click the corresponding link.
   4. Click on the "Download R for (Mac) OS X" link at the top of the page.
   5. Click on the file containing the latest version of R under "Files."
   6. Save the .pkg file, double-click it to open, and follow the installation instructions.
   7. Now that R is installed, you need to download and install RStudio.
    
##### To install RStudio
   1. Use the link below to install RStudio Desktop  
   https://www.rstudio.com/products/rstudio/download/
   
### Step 2: Open RStudio and create a new project 
1. File --> New Project 
2. Existing Directory 
   - choose folder that you saved included files to
3. Create Project
4. File --> New File --> R Script

### Step 3: Install neccessary packages

Copy and paste the following text into your R script, then click "Run"

    install.packages("shiny")   
    install.packages("shinythemes")    
    install.packages("DT")  
    install.packages("leaflet")  
    install.packages("leaflegend")  
    install.packages("readxl")    
    install.packages("raster")  
    install.packages("tidyverse")  
    install.packages("tigris")  
    install.packages("shinycssloaders")  
    install.packages("htmltools")  
    install.packages("rgdal")  
    install.packages("reshape2")  
    install.packages("viridis")  
    install.packages("data.table")  
    install.packages("shinyjs")  
    install.packages("shinycssloaders")  
    install.packages("viridis")  
    install.packages("viridisLite")  
    install.packages("shinydashboard")  
    install.packages("pwr")  
    install.packages("shinyWidgets")  
    install.packages("hablar")  

### Step 4: Copy the raw code app.R

Open the file "app.R" in RStudio, and press the "Run App" button on the top right of the script.

#### NRMP Data Cleaning App should open in your web browser

![alt text](https://github.com/AmyJDavis/NRMPDataCleaning/blob/main/NRMP%20MIS%20Data%20Cleaning%20App.png?raw=true)  
Image 1. Home screen of NRMP MIS Data Cleaning App.

### Step 5: Select and add dataset to shiny app

Location Check: map of MIS samples, table of samples with county location errors, summary of location issues

Rabies Check: proportion of samples with rabies results, summary of test results issues

Fate Check: distribution of different fate types, fate-method combinations

Serology: serology information, distribution of VNA results by interpretation

Summary of Errors: summary of errors in the data, table of data errors by code

Error Definitions: table of error codes and their corresponding definitions

### Step 6: Download the datafile with errors 

Click the "Download data with errors" button to save the data file.
