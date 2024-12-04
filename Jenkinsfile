pipeline {
    agent any  // This specifies the agent (i.e., where the job will run)

    tool{
        maven 'maven_3_9_9'
    }
    stages {
        stage('Checkout') {
            steps {
                // Pull the code from the repository
                checkout scm
            }
        }

        stage('Build and Install') {
            steps {
                script {
                    // Run Maven clean install
                    bat 'mvn clean install'  // Unix/Linux command
                    // On Windows, you would use 'bat "mvn clean install"'
                }
            }
        }
    }
}
