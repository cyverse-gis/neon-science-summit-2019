# neon-science-summit-2019
Example Notebooks for NEON Science Summit Planet Labs breakout session

# Copy samples

Clone this repository into the running instance

```
git clone https://github.com/cyverse-gis/neon-science-summit-2019
```

# Downloading NEON Data with R Shiny

## Run Shiny app in RStudio

Clone the repository to your computer or VM

```
git clone https://github.com/cyverse-gis/neon-shiny-browser
```

Change your RStudio working directory to the downloaded location

```
getwd()
setwd("~/neon-shiny-browser")
```

Load the Shiny Library and run the app

```
library(shiny)
runApp()
```

Note - you may need to install additional dependencies for the app on your local computer first.

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

# Downloading Planet Labs data with Jupyter Lab 

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

(2) Log into the Discovery Environment: https://de.cyverse.orgh

(3) Open the Apps tab and search for "Jupyter" or "Planet" and find the corresponding public apps

(4a) Launch a Jupyter Lab with Planet Labs and Google Earth Engine tools pre-built 

Note: Access to Planet data requires a [Planet Labs Account](https://planet.com) 

<a href="https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=067d4a4b-bedb-4034-baba-2f59c15e0463&app-id=1d35dc48-eb93-11e9-b6b7-008cfa5ae621" target="_blank"><img src="https://de.cyverse.org/Powered-By-CyVerse-blue.svg"></a>
