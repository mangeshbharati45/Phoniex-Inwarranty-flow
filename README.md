# Postman API Automation Integration with github Actions #

This Repository is a demonstration for POC for integrating postman tests with github actions. The test are written in postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra

Github Actions will trigger project execution on push to the main branch. You can also execute project manually using workflow-dispatch. The project runs on scheduled time with help of cron job

The HTML report is archieved and kept in artifact section for team to dowmload along with they can view report directly from github page : https://mangeshbharati45.github.io/Phoniex-Inwarranty-flow/


## Test Stack ##
1. Postman
2. Node.js 
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SNTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 Instances for Self hosted github runner


## Github Pages ##
You can directly view the latest report of the Postman Test at the Github page link : https://mangeshbharati45.github.io/Phoniex-Inwarranty-flow/


## How to run the project ##
You can run the project on your local system for that:
1. Clone the project on Local System: https://github.com/mangeshbharati45/Phoniex-Inwarranty-flow.git
2. Install Node.js and NPM from https://nodejs.org/en
3. Install Newman: npm install -g newman
4. Install Newman-reporter-htmlextra: npm install -g newman-reporter-htmlextra
5. Run the newman Command :
              newman run 'Inwarranty-flow Collection.postman_collection.json' \  
             -e QA.postman_environment.json \
             -d testData.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
   ## HTML Report ##
   The Report will be created in the newman folder
