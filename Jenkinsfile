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
                 // Run Maven on a Unix agent.
                sh "mvn clean package -e"
                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
