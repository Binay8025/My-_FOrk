pipeline {
    
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
