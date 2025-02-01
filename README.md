<h1 size= 10px> DevOps CI/CD Workflow </h1>

<p># Overview:</p>
This repository includes Software university task to create a CI/CD pipeline that automates the following stages:

<p> Build & Test:</p> Install dependencies, set up Node.js, run integration tests.
Security Test: Run npm audit to check for vulnerabilities after the build and test job passes.
The pipeline ensures that code is built, tested, and secured before deployment, with security checks being enforced in the pipeline.

<p>Workflow </p>
1. Build and Test Stage
Install Node.js dependencies: This stage ensures that all necessary dependencies are installed for your Node.js application.
Install Node.js version: The correct version of Node.js will be installed for your application using the setup-node action.
Run integration tests: This step will execute all defined integration tests to ensure that the application behaves as expected.
Build and Test Job Steps:

<p>Clone the GitHub repository.</p>
Set up Node.js (version 20).
Install dependencies (npm install).
Run all integration tests (npm run test).
If this stage fails, the pipeline will not proceed to the security testing job.

<p>2. Security Test Stage</p>
Once the build and test job passes, the Security Test job will be triggered. This step runs npm audit to check for vulnerabilities in your dependencies.

Run npm audit: This command checks the project’s dependencies for known security vulnerabilities.
Fail the build if high vulnerabilities are found: If there are any high-severity vulnerabilities, the workflow will be marked as failed.
Security Test Job Steps:

Run the npm audit command.
Generate an audit report and check for high-severity vulnerabilities.
Fail the job if high-severity vulnerabilities are detected.
3. Deploy Stage (Optional)
After the security tests pass (if applicable), the final step would be deployment. This would depend on your specific deployment requirements (e.g., deploying to a server, cloud provider, etc.).
