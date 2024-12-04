pipeline {
    agent any  // Runs on any available Jenkins agent

    environment {
        // Define environment variables
        MAVEN_HOME = 'E:apache-maven-3.9.9\bin\mvn' // Path to Maven installation (adjust as necessary)
       
    }

    tools {
        maven 'Maven 3'  // Use Maven 3 tool configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the code from the Git repository
                    git branch: 'master', url: 'https://github.com/Binay8025/My-_FOrk.git'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Run Maven build
                    echo 'Building the project using Maven...'
                    sh "'${MAVEN_HOME}/bin/mvn' clean install"
                }
            }
        }

    }   
    
}
