# sonarqube-report-downloader

## Introduction

This python script will download your SonarQube vulnerability SAST report as a json file. This script works for both Sonarcloud (SaaS) and SonarQube (on-premise). 

## Pre-Requisites

* You must have Python installed in your environment. If you don't have Python installed, please do so by visiting the Python download site [here](https://www.python.org/downloads/).
* You will need to run the script via your terminal or command prompt. 


## Required environment variables

### `SONARQUBE_HOST_URL`
Example values: `https://sonarcloud.io` or `http://localhost:9000`

### `SONARQUBE_TOKEN`
Generate this token at by following the instruction [here](https://docs.sonarsource.com/sonarqube/9.8/user-guide/user-account/generating-and-using-tokens/#generating-a-token)

### `SONARQUBE_ORG`
Your Sonarcloud Org ID. If you are using SonarQube, enter `none`

### `SONARQUBE_PROJECT`
Your Sonarqube project key

### `BRANCH`
The branch name. 
For example: `main`

### `REPORT_PATH`
Name of the output report
For example: `sonar_report.json`



## Sample command to download a report tied to a branch:
```
SONARQUBE_HOST_URL=https://sonarcloud.io \
SONARQUBE_TOKEN=XXX \
SONARQUBE_ORG=antonychiu2 \
SONARQUBE_PROJECT=antonychiu2_wf-examples-sonar \
BRANCH=main \
REPORT_PATH=sonar_report.json \
python sonarqube_download_report.py
```

## Sample command to download a report tied to a PR:
```
SONARQUBE_HOST_URL=https://sonarcloud.io \
SONARQUBE_TOKEN=XXX \
SONARQUBE_ORG=antonychiu2 \
SONARQUBE_PROJECT=antonychiu2_wf-examples-sonar \
PULL_REQUEST_ID=13 \
REPORT_PATH=sonar_report.json \
python sonarqube_download_report.py
```

## Sample command to download a SAST report from SonarQube (on-premise):
```
SONARQUBE_HOST_URL=http://local-ubuntu-vm:9000 \
SONARQUBE_TOKEN=XXX \
SONARQUBE_ORG=none \
SONARQUBE_PROJECT=webgoat-local \
BRANCH=main \
REPORT_PATH=sonar_report.json \
python sonarqube_download_report.py
```


