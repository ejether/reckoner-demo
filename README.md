# reckoner-demo
## Requirements
1. Kubernetes cluster with context configured
1. Helm 3 installed and on your path
1. python 3.8 or greater 
1. virtualenv install (optional)

## Create Venv
1. `python3 -m virtualenv reckoner`
1. `. reckoner/bin/activate`

## Install `reckoner`
1. `pip install reckoner`
1. (Binary install also available, but it is flaky https://github.com/FairwindsOps/reckoner/releases/tag/v4.3.1)

## Run A Single Chart
1. `reckoner plot course.yml --only redis-one` 

## Run A Single Chart with verbose logging
1. `reckoner plot course.yml --only redis-one --log-level=debug`

## Prep Env (or try without to see what the error is)
1. `export REDIS_TWO_PASSWORD=redis-password`
1. `export EXTRA_EXTERNAL_DNS_FILE=extra-external-dns-values.yml`

## Run all Charts
1. `reckoner plot course.yml --run-all`

## Investigate other Commands
1. `reckoner --help`
1. `reckoner plot --help`
1. `reckoner update --help`
1. `reckoner template --help`


## More Resources
1. https://github.com/FairwindsOps/reckoner-demo
1. https://github.com/FairwindsOps/reckoner/tree/master/docs


### Repo Contents
1. `course.yml`: The main configuration file
1. `foo`: default helm chart to demonstrate local helm chart
1. `external-dns-values.yml`: file of values for external-dns release
1. `extra-external-dns-values.yml`: file of values for external-dns release, but set in an environment variable
