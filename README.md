# sonarqube-report-downloader

Example command to download a report tied to a branch:
```
SONARQUBE_HOST_URL=https://sonarcloud.io \
SONARQUBE_TOKEN=XXX \
SONARQUBE_ORG=antonychiu2 \
SONARQUBE_PROJECT=antonychiu2_wf-examples-sonar \
BRANCH=main \
REPORT_PATH=sonar_report.json \
python sonarqube_download_report.py
```

Example command to download a report tied to a PR:
```
SONARQUBE_HOST_URL=https://sonarcloud.io \
SONARQUBE_TOKEN=XXX \
SONARQUBE_ORG=antonychiu2 \
SONARQUBE_PROJECT=antonychiu2_wf-examples-sonar \
PULL_REQUEST_ID=13 \
REPORT_PATH=sonar_report.json \
python sonarqube_download_report.py
```
