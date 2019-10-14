# neon-science-summit-2019
Example Notebooks for NEON Science Summit Planet Labs breakout session

# Cloning a GitHub Repository

Clone this repository - there are example .ipynb notebooks for you to work with. 

```
git clone https://github.com/cyverse-gis/neon-science-summit-2019
```

# Find and download NEON data with our R Shiny App

## Run the Shiny app in RStudio

Clone the Shiny App repository 

```
git clone https://github.com/cyverse-gis/neon-shiny-browser
```

Change your RStudio working directory to the location of the app:

```
getwd()
setwd("~/neon-shiny-browser")
```

Load Shiny and run the app (note - the app has numerous spatial dependencies which must also be installed if running on a local machine, this can take some time).

```
library(shiny)
runApp()
```

<p align="center"><img src='https://github.com/cyverse-gis/neon-science-summit-2019/blob/master/gif/RStudio_NEON_Shiny.gif?raw=true' width='750'></p>

## Run Shiny app in CyVerse

Select the NEON-Shiny-Browser App in CyVerse.

Browse and download data to the Data Store.

View downloaded data in your home folder `/analyses`

## Run Shiny app with Docker locally or on a Virtual Machine

Download from DockerHub:

```
docker pull cyversevice/shiny-geospatial:neon-shiny-browser
```

Or just run the app:

```
docker run -it --rm -p 3838:3838 -e REDIRECT_URL=http://localhost:3838 -v ~/NEON_Downloads:/NEON_Downloads cyversevice/shiny-geospatial:neon-shiny-browser
```

# Download Planet Labs data with Jupyter Lab 

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3484160.svg)](https://doi.org/10.5281/zenodo.3484160)

Launch with [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/samapriya/neon-science-summit-2019/master)

Citation:

```
Samapriya Roy. (2019, October 14). samapriya/neon-science-summit-2019: neon-science-summit-2019 (Version 0.1). Zenodo.
http://doi.org/10.5281/zenodo.3484160
```

## Run Jupyter Lab on your own computer

You will need to install numerous dependencies for running the Lab

## Run Jupyter Lab with Docker

```
docker run -it --rm -v /$HOME:/app --workdir /app -p 8888:8888 -e REDIRECT_URL=http://localhost:8888 cyversevice/jupyterlab-scipy:planet-latest
```

Note you may need to mount the location of your NEON Data when you start the container

```
-v ~/NEON_Downloads:/NEON_Downloads
```

# Run Jupyter Lab using CyVerse VICE

CyVerse hosts a data science workbench called the Discovery Environment. You can launch visual and interactive compute environments (VICE) containers from the DE. 

Steps:

(1) Register for CyVerse https://user.cyverse.org/

(2) Log into the Discovery Environment: https://de.cyverse.org

(3) Open the Apps tab and search for "Jupyter Lab Planet" and find the corresponding public app, or use this Quick Launch <a href="https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=3915f0c6-d817-40b3-8475-2a7b93d928a8&app-id=1d35dc48-eb93-11e9-b6b7-008cfa5ae621" target="_blank"><img src="https://de.cyverse.org/Powered-By-CyVerse-blue.svg"></a>



<p align="center"><img src='https://github.com/cyverse-gis/neon-science-summit-2019/blob/master/gif/DE_launch.gif?raw=true' width='750'></p>
