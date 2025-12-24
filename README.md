# Postman API Automation Integration with Github Actions

This repository is a demostration for POC for integrating postman tests with github actions. The test are written in postamn and they exceuted on the VM with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to the main branch. You can also execute the project manually workflow_dispatch. The projects run on the scheduled time on the crons job.

The html reports are archived and kept in the arifact sections for the team to download it. Along with that they can view the report directly from the github page : https://swatirshetty.github.io/Phoenix-Inwarranty-Flow/.
The latest report is emailed to the team members using GMAIL SMTP.


## Tech Stack ##
1. Postman
2. nodejs 24v
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven testing
9. AWS-EC2 instance for self hosted github runner.


## GitHub Pages ##
You can directly view the latest test report of the Postman Test at the GitHub Page : https://swatirshetty.github.io/Phoenix-Inwarranty-Flow/

## How to run the project ##
you can run the project on your local system for that:
1. Clone the Project on the Local system:  https://github.com/swatirshetty/Phoenix-Inwarranty-Flow.git
2. Install nodejs and npm https://nodejs.org/en
3. Install newman using npm install -g newman
4. Install newman --reporter-htmlextra npm install -g newman-reporter-html
5. Run the newman command:
               newman run 'Inwarranty-flow Collection copy 2.postman_collection.json' \
              -e QA.postman_environment.json \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html

   
   
  
