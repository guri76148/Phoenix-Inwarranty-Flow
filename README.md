# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating Postman tests with github actions. The Tests are written in Postman and they are executed on the VM (Amazon EC2) created with self-hosted github runner with the help of newman and newman-repoter-htmlextra.
Github Actions will trigger this project execution on every push to main branch. You can also execute this project manually using workflow_dispatch. The Project also runs on a scheduled time with help of cron job.

The HTML is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from github page: https://guri76148.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP.

## Tech Stack ##
1. Postman
2. Nodejs 22
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for selh-hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman Test at Github page link : https://guri76148.github.io/Phoenix-Inwarranty-Flow/

## How to run the Project ##
You can run the project on the local machine:
1. Clone the project : https://github.com/guri76148/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from : https://nodejs.org/en
3. Install Newman : $ npm install -g newman
4. Install Newman-Reporter-Htmlextra : npm install -g newman-reporter-htmlextra
5. Run the newman command : newman run 'inwarranty-flow Collection.postman_collection.json' \  
                            -e QA.postman_environment.json \
                            -d testdata.csv \
                            -r cli,htmlextra \
                            --reporter-htmlextra-export ./newman/index.html


## HTML Report ##
