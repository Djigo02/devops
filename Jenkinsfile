pipeline {
    agent any

    stages {
        stage('Git') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/Djigo02/devops.git'
            }
        }
        stage('maven validate') {
            steps {
                 // Run Maven on a Unix agent.
                sh "mvn validate"
                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
