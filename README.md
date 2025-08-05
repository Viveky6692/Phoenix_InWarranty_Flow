# Postman API Automation integration with Guthub Actions #

This Repository is a demonstration for POC for integrating postman tests with the github actions. The tests are written in postman and they are executed with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. 
The project runs on the schecuduled time with the help of cron jobs.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page.  https://viveky6692.github.io/Phoenix_InWarranty_Flow/.
The latest report is emailed to the team members using GMAIL SMTP. 

## About Me ##
My name is Vivek yadav having QA experience in Banking and healthcare staffing. i am having 3 years of experience in Automation tetsing. 

## Testing Coverage ##
1. Happy path testing
2. Negative testing
3. Edge Case testing
4. Token testing
5. Data Driven Testing with CSV
6. Schema Validation
7. Secrets managements with Github Secrets

## Tech Stack ##
1. Postman
2. Node Js 22
3. newman
4. newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github pages
8. csv file for data driven testing
9. AWS EC2 instance for self hosetd github runner

## Github pages ## 
You can directly view the latest html reports for the postman tests at the Github pages. https://viveky6692.github.io/Phoenix_InWarranty_Flow/.

## HTML report ## 
The report will be created in the newman folder
![Postman Report](https://raw.githubusercontent.com/Viveky6692/Phoenix_InWarranty_Flow/Static-Content/HTML_report_snapshot.PNG)

## Project Structure ##

```
Collection Export Data
│  ├─ Jatin_Inwarranty-flow Collection.postman_collection.json    # Postman Collection File 
│  ├─ Jatin_QA.postman_environment.json    # Environement File
│  └─ testData.csv                         # Test Data File


```

## How to run the Project? ##
You can run the project on the local system for that:
1. Clone the project on local system: https://github.com/Viveky6692/Phoenix_InWarranty_Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman $ using ```npm install -g newman```
4. install newman-reporter-htmlextra using ```npm install -g newman-reporter-htmlextra```
5. Run the newman command: newman run In_Warranty_Newman_CLI2.postman_collection \  
            -e QA.postman_environment.json \
            -d testData.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export newman/index.html # index html report is stored



