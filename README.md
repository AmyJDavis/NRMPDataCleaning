
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

The following file is the R script you should save in the same working directory as specified above. Open this script in R via RStudio to run the shiny app (used in Step 4)  
1.	app.R

## Step by Step to Launch App From R

### Step 1: Download R and RStudio (if both are already installed proceed to Step 2)

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
   7. Now that R is installed, you need to download and install RStudio. 
   
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

### Step 4: Run the app from R using the script: app.R

Open the file "app.R" in RStudio, and press the "Run App" button on the top right of the script.

#### NRMP Data Cleaning App should open in your web browser

![alt text](https://github.com/AmyJDavis/NRMPDataCleaning/blob/main/NRMP%20MIS%20Data%20Cleaning%20App.png?raw=true)  
Image 1. Home screen of NRMP MIS Data Cleaning App.

### Step 5: Select and add dataset to shiny app

The app provides several tabs to visually explore issues with the data.  It is not necessary to examine these.  You can proceed directly to Step 6 and download the data with error codes.  The codes are provided on the "Error Definitions" tab.  You can download the PDF of the data errors on your computer to get descriptions on the errors.  If you are interested in visualizing your data and errors click through the following tabs. 

1. Location Check tab: This tab provides a map of MIS samples, the points are color coded and are red if the county in the MIS record does not match the county where the latitude/longitude data show the location. There is also a table showing the samples with county location errors. Lastly, there is a summary box showing the number of location issues.

2. Rabies Check tab: This tab shows the number of samples that are awaiting results (either rabies results, titer results, or results from other samples) shown in yellow compared to the number of samples with test results provided, shown in purple. The summary boxes along the bottom show the number of results that are needed.  The errors for needing these samples to be filled in will only show after either 30 days or 1 year has elapsed and no results are provided. 

3. Fate Check tab: This tab shows the distribution of different fate types in the data in a pie chart.  Also provided is a table of fate-method combinations.  This information is helpful as certain fate-method combinations should not occur and this can help point those out.

4. Serology tab: This tab will only have information if there is serology information collected in the data set.  The box shows the number of samples with serology information. The figure shows the distribution of VNA results (VNA values) based on if they were classified as positive or negative. 

5. Summary of Errors tab: This tab shows the summary of errors in the data both in a plot and table form.  It gives the number of each type of errors that is present in the data set.   This can be helpful to identify where common problems are in data reporting for your dataset. 

6. Error Definitions tab: This tab has a PDF table of error codes and their corresponding definitions.  This should be downloaded to your computer so help with data cleaning. 

### Step 6: Download the datafile with errors 

Click the "Download data with errors" button to save the data file.
