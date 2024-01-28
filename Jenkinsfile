pipeline {
    agent any

    tools {
      maven 'maven'
      git 'Default'
    }

    stages {
        stage('Git') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/Djigo02/devops.git'
            }
        }
        stage('maven clean') {
            steps {
                 script {
                    sh 'mvn clean package -e'
                }
            }
        }
    }
}
