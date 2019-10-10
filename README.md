# neon-science-summit-2019
Example Notebooks for NEON Science Summit Planet Labs breakout session

# Run spatial analyses using CyVerse VICE

(1) Register for CyVerse https://user.cyverse.org/

(2a) Launch Jupyter Lab with Google Earth Engine in Discovery Environment

<a href="https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=694ae50d-7725-46b6-82a8-a04755c3e43a&app-id=1f5e7f3a-e46c-11e9-870d-008cfa5ae621" target="_blank"><img src="https://de.cyverse.org/Powered-By-CyVerse-blue.svg"></a>

(2b) Launch Jupyter Lab with Planet Labs in Discovery Environment

Requires [Planet Labs Account](https://planet.com) with API Key

<a href="https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=25862506-3ffe-4867-8e2b-664d9df47ce3&app-id=0c91c2b0-eab9-11e9-a785-008cfa5ae621" target="_blank"><img src="https://de.cyverse.org/Powered-By-CyVerse-blue.svg"></a>

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
## Run Jupyter Lab with CyVerse
