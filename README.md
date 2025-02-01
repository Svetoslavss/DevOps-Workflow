# DevOps-Workflow
Software university , task create CI/CD workflow for build and test and deploy

<p> - Build and test: for instaling the node app dependencies , install node version and run all integration tests needed. </p>
<p> - Once the job passes it will turn on the security_test job so it will run the npm audit stage for the security tests. If Job one fails , job two will not start. </p>

