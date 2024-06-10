Prerequisites

Before starting, I ensured the following:
- An Ubuntu server set up and running.
- Jenkins installed and configured on the Ubuntu server.
- Docker and Kubernetes installed on the server.
- Ansible installed for configuration management and testing.
- Basic knowledge of Jenkins, Docker, Kubernetes, and Ansible.

Steps

1. Set Up Jenkins

Installed Jenkins
   - Installed Jenkins on the Ubuntu server and ensured it was running.

Configured Jenkins
   - Accessed Jenkins through a web browser and completed the initial setup wizard, including installing recommended plugins and creating an admin user.

 Set Up Docker and Kubernetes

Installed Docker
   - Set up Docker on the Ubuntu server to facilitate containerization of the application.

*Installed Kubernetes
   - Installed Kubernetes tools on the server to manage containerized applications.

Create and Use Manifest Files

Created Kubernetes Manifest Files
   - Defined deployment and service configurations in YAML files (`deployment.yaml` and `service.yaml`).
   - Stored these manifest files in a version control repository.

4. Configure Jenkins Pipeline
Set Up Jenkins Pipeline**:
   - Created a new Jenkins pipeline job.
   - Configured the pipeline to pull the code and manifest files from the version control repository.
   - Wrote a Jenkinsfile with stages for building the Docker image, pushing it to a Docker registry, deploying to Kubernetes, and running Ansible tests.

Jenkins file Overview:
- Checkout Stage: Pulled the latest code and manifest files from the repository.
- Build Docker Image Stage: Built the Docker image for the application.
- Push Docker Image Stage: Pushed the Docker image to a Docker registry.
- Deploy to Kubernetes Stage: Deployed the application to a Kubernetes cluster using the manifest files.
- Run Ansible Tests Stage: Executed an Ansible playbook to test the deployed Docker image.

5. Test Docker Image with Ansible

 Executed Ansible Tests
   - Ensured the Jenkins pipeline included a stage to run the Ansible playbook, validating the deployment.

 Verify the Deployment

Checked Kubernetes Deployment
   - Verified the successful deployment of the application to the Kubernetes cluster.

Reviewed Jenkins Pipeline
   - Ensured all stages in the Jenkins pipeline completed successfully.

Validated Ansible Test Results
   - Confirmed that the Ansible playbook executed successfully and all tests passed.

Conclusion

This project demonstrated a comprehensive approach to deploying Kubernetes and Docker files using Jenkins on an Ubuntu server, with a strong emphasis on establishing a CI/CD pipeline. The deployment process was automated using Jenkins pipelines, manifest files defined the Kubernetes resources, and Ansible ensured the Docker image's functionality through rigorous testing. This setup facilitated efficient and reliable deployment and testing of containerized applications, highlighting the importance of CI/CD practices in modern software development.
