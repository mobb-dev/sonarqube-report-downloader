# sonarqube-report-downloader

## Required environment variables

`SONARQUBE_HOST_URL`
Example values: 
`https://sonarcloud.io`
`http://localhost:9000`

`SONARQUBE_TOKEN`
Generate this token at by following the instruction [here](https://docs.sonarsource.com/sonarqube/9.8/user-guide/user-account/generating-and-using-tokens/#generating-a-token)

`SONARQUBE_ORG`
Your Sonarcloud Org ID. If you are using SonarQube, enter `none`

`SONARQUBE_PROJECT`
Your Sonarqube project key

`BRANCH`
The branch name. 
For example: `main`

`REPORT_PATH`
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
