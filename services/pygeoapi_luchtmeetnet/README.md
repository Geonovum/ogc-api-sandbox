# Demo service for pygeoapi - Luchtmeetnet

Runs latest GitHub `main` branch of `pygeoapi` using
its [Docker Image from DockerHub](https://cloud.docker.com/u/geopython/repository/docker/geopython/pygeoapi).
with a [local config file](local.config.yml).

**This API is for demonstration purposes only, in the context of Geonovum's API Testbed.**

## Data

The data of the stations is taken from RIVM's Luchtmeetnet API. It is constructed from the stations, station details and uses references to measurements data. Data is converted to GeoJSON.

## Deployment

This service is automatically (re)deployed if anything within this directory or its subdirs changes
when committed/pushed.

A GitHub Action invokes an Ansible Playbook.
See the following deployment files:

* [GitHub Action](../../.github/workflows/deploy.pygeoapi_luchtmeetnet.yml)
* [Ansible Playbook](../../ansible/deploy.yml)

The Ansible Playbook can also be invoked directly.
