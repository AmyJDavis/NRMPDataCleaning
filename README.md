# NRMP Data Cleaning
Below is a step by step guide on how to open and use the NRMP Data Cleaning App. The App can be accessed by link, or by running the program through R/RStudio. 

## Opening App from R
### Step 1: Download R (if already downloaded proceed to Step 2)
#### Submit IT ticket requesting to have R and R Studio (latest versions) installed 
#### -OR-
#### If you administrative privileges on your computer, do either of the following:
##### Windows Users - to install R
###### 1. Open an internet browser and go to www.r-project.org.
###### 2. Click the "download R" link in the middle of the page under "Getting Started."
###### 3. Select a CRAN location (a mirror site) and click the corresponding link.  
###### 4. Click on the "Download R for Windows" link at the top of the page.  
###### 5. Click on the "install R for the first time" link at the top of the page.
###### 6. Click "Download R for Windows" and save the executable file somewhere on your computer.  Run the .exe file and follow the installation instructions.      
##### Mac Users - to install R
###### 1. Open an internet browser and go to www.r-project.org.
###### 2. Click the "download R" link in the middle of the page under "Getting Started."
###### 3. Select a CRAN location (a mirror site) and click the corresponding link.
###### 4. Click on the "Download R for (Mac) OS X" link at the top of the page.
###### 5. Click on the file containing the latest version of R under "Files."
###### 6. Save the .pkg file, double-click it to open, and follow the installation instructions.
###### 7. Now that R is installed, you need to download and install RStudio.
### Step 2: Open R and download neccessary packages
#### install.packages("shiny") 
#### install.packages("shinythemes")
#### install.packages("DT")
#### install.packages("leaflet")
#### install.packages("leaflegend")
#### install.packages("readxl")
#### install.packages("raster")
#### install.packages("tidyverse")
#### install.packages("tigris")
#### install.packages("shinycssloaders")
#### install.packages("htmltools")
#### install.packages("rgdal")
#### install.packages("reshape2")
#### install.packages("viridis")
#### install.packages("data.table")
#### install.packages("shinyjs")
#### install.packages("shinycssloaders")
#### install.packages("viridis")
#### install.packages("viridisLite")
#### install.packages("shinydashboard")
#### install.packages("pwr")
#### install.packages("shinyWidgets")
#### install.packages("hablar")
### Step 3: Copy the raw code from app.R
#### Go to AmyJDavis/NRMPDataCleaning and click on app.R in the repository
#### In the top right of the box containing the code, click "copy raw contents"
#### Paste this into R and run the code
#### NRMP Data Cleaning App should open




