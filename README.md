# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman tests with github actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on the schedule time with the help of the cron job

The Html report Archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from github page : https://testdynemorahul.github.io/Phoenix-Inwarranty-Flow-Collection/.
The latest report is mailed to the team member using GMAIL SMTP.

## About Me ##
Hi My name is Rahul Prajapati. I have 6 years of experiance in Automation and Manual Testing. My Skillset includes UI Automation with Selemium Webdriver and for API Testing I use RestAssured and Postman. You can connect with me over:(https://www.linkedin.com/in/rahul-prajapati-77893b128/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing
3. Token Testing
4. Data driven testing with csv
5. Schema Validation
6. Secrets management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. GMAIL SMTP
7. Github pages
8. csv for data driven testing
9. AWS EC2 Instances for Self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman from the Github page link:https://testdynemorahul.github.io/Phoenix-Inwarranty-Flow-Collection/

## HTML Report ##
The Report will be created in the newman folder

![Postman Report](https://raw.githubusercontent.com/testdynemorahul/Phoenix-Inwarranty-Flow-Collection/Static-Content/Newman-Report.PNG)

## Project Structure  ##
```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection.postman_collection.json # Collection file
├─ QA Copy.postman_environment.json # Environment file
└─ testData.csv # Test data file

```
## How To Run the Project? ##
You can run the project on your local system for that:
1. Clone the project on local system: https://github.com/testdynemorahul/Phoenix-Inwarranty-Flow-Collection.git
2. Install Nodesjs and NPM from: https://nodejs.org/en
3. Install Newman using command ```npm install -g newman```
4. Install Newman-Reporter-extra using command: ```npm install -g newman-reporter-htmlextra```
5. To execute the project Run the newman command:
```
             newman run 'Inwarranty-flow Collection.postman_collection.json' \ 
            -e 'QA Copy.postman_environment.json' \
            -d testData.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html

```


