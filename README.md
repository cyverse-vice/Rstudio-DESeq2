[![Project Supported by CyVerse](https://img.shields.io/badge/Supported%20by-CyVerse-blue.svg)](https://learning.cyverse.org/projects/vice/en/latest/) [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3246938.svg)](https://doi.org/10.5281/zenodo.3246938) [![license](https://img.shields.io/badge/license-GPLv2-blue.svg)](https://opensource.org/licenses/GPL-2.0)

# rstudio-DESeq2 1.0



[![CircleCI](https://circleci.com/gh/cyverse-vice/Rstudio-DESeq2.svg?style=svg)](https://circleci.com/gh/cyverse-vice/Rstudio-DESeq2)[![DockerHub](https://img.shields.io/badge/DockerHub-brightgreen.svg?style=popout&logo=Docker)](https://hub.docker.com/r/cyversevice/rstudio-base)


quick launch | tag | size | metrics | build | status |  
------------ | --- | ---- | ------- | ------|--------|
<a href="https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=1444198d-068f-4cf1-a3d1-df30e6d678f2&app-id=58f9a86c-2a74-11e9-b289-008cfa5ae621" target="_blank"><img src="https://de.cyverse.org/Powered-By-CyVerse-blue.svg"></a> |[![TAG](https://images.microbadger.com/badges/version/cyversevice/shiny-verse.svg)](https://microbadger.com/images/cyversevice/Rstudio-DESeq2) | [![SIZE](https://images.microbadger.com/badges/image/cyversevice/Rstudio-DESeq2.svg)](https://microbadger.com/images/cyversevice/Rstudio-DESeq2) | [![Docker Pulls](https://img.shields.io/docker/pulls/cyversevice/Rstudio-DESeq2?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/Rstudio-DESeq2) | [![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/cyversevice/Rstudio-DESeq2?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/Rstudio-DESeq2) | [![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/cyversevice/Rstudio-DESeq2?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/Rstudio-DESeq2)


# Instructions

## Run this Docker locally or on a Virtual Machine

To run these containers, you must first pull them from DockerHub

```
docker pull cyversevice/rstudio-verse:latest
```

```
docker run -it --rm -v /$HOME:/app --workdir /app -p 8787:80 -e REDIRECT_URL=http://localhost:8787 cyversevice/rstudio-verse:latest
```

The default username is `rstudio` and password is `rstudio1`. To reset the password, add the flag `-e PASSWORD=<yourpassword>` in the `docker run` statement.

## Build your own Docker container and deploy on CyVerse VICE

This container is intended to run on the CyVerse data science workbench, called [VICE](https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/index.html). 

Unless you plan on making changes to this container, you should just use the existing launch button above. 

###### Developer notes

To build your own container with a Dockerfile and additional dependencies, pull the pre-built image from DockerHub:

```
FROM cyversevice/rstudio-verse:latest
```

Follow the instructions in the [VICE manual for integrating your own tools and apps](https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/developer_guide/building.html).
