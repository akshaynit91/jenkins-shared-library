# Jenkins Shared Library      

## Description

This Jenkins Shared Library provides a collection of reusable Groovy scripts and functions to streamline and enhance your Jenkins pipeline configurations. With this library, you can simplify your Jenkinsfile, promote best practices, and improve the maintainability of your CI/CD pipelines.

## Features   

- Commonly used utility functions and methods.
- Predefined pipeline stages for common tasks.
- Easy integration into your Jenkins pipelines.

## Installation   

## Usage of the Jenkins Shared Library

To utilize the features provided by this Jenkins Shared Library in your Jenkins pipeline, follow these steps:

1. **Import the Library:**

   At the beginning of your Jenkinsfile, import the shared library using the `@Library` annotation. Replace `'jenkins-shared-library'` with the actual name you configured in Jenkins.

   ```groovy
   @Library('jenkins-shared-library') _


##  Usage   

To use the Jenkins Shared Library in your Jenkins pipeline, import it at the beginning of your Jenkinsfile:


@Library('jenkins-shared-library') _

Then, you can call functions and stages from the library in your pipeline script:


      pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    myLibrary.buildStep()
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    myLibrary.testStep()
                }
            }
        }
        
        // Add more stages as needed
    }
    
    post {
        always {
            script {
                myLibrary.cleanup()
            }
        }
    }
}



## Support     

If you encounter any issues, have questions, or want to contribute to this project, please open an issue on the GitHub repository.

## Contributing   
We welcome contributions! If you want to contribute to this project, please follow our contribution guidelines.

## Authors and Acknowledgment   


Author: **Akshay Singh**

We would like to thank the Jenkins community for their inspiration and support in building this shared library.

This project is licensed under the MIT License.

## Project Status

This project is actively maintained and open to contributions. Feel free to reach out if you'd like to become a maintainer or if you have any questions or concerns.
