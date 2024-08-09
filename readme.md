
---

# Spring PetClinic Jenkins Pipeline

## Overview

This repository showcases a Jenkins pipeline designed to automate the build and deployment process for the **Spring PetClinic** application. The pipeline is tailored to efficiently handle the continuous integration and deployment (CI/CD) of the application to a remote Tomcat server, emphasizing best practices in DevOps.

## Project Details

The **Spring PetClinic** application is a widely recognized sample project built with Spring Boot. While the core application is pre-existing, this repository highlights the creation and management of a Jenkins pipeline to demonstrate CI/CD capabilities.

### Key Modifications

- **Packaging Configuration**: The `pom.xml` file has been manually configured to produce a WAR file instead of the default JAR file, ensuring compatibility with the deployment environment.

## Jenkins Pipeline Overview

The Jenkins pipeline defined in this project automates the following key stages:

1. **Checkout**:
   - The pipeline pulls the latest code from the `main` branch of the repository.

2. **Build**:
   - Uses Maven Wrapper (`mvnw`) to clean and package the Spring PetClinic application into a WAR file.

3. **Deploy**:
   - The pipeline securely transfers the WAR file to a remote Tomcat server and deploys it, ensuring the application is live and accessible.

### Prerequisites

- **Jenkins**: Properly configured and integrated with the necessary plugins.
- **Apache Tomcat**: Running on the target virtual machine (VM) with appropriate permissions set up.
- **SSH Access**: Jenkins must be configured with SSH credentials (`jenkins-key`) to securely connect to the remote VM.
- **Maven Wrapper**: Included in the project for consistent build behavior across different environments.

## Running the Pipeline

1. **Pipeline Setup**:
   - Create a new pipeline job in Jenkins, linking it to this repository.
   - Configure Jenkins to use the provided `Jenkinsfile` for pipeline execution.

2. **Execution**:
   - Trigger the pipeline manually or automatically based on specific events (e.g., code push to `main`).

3. **Deployment**:
   - The pipeline will handle the build and deployment of the application to the Tomcat server on the specified VM.

## Conclusion

This project demonstrates a practical application of Jenkins for automating the CI/CD pipeline. It highlights my ability to configure and manage Jenkins pipelines, as well as my proficiency in automating the deployment of Java applications to remote environments.

## License

This project is licensed under the [MIT License](LICENSE).

---
