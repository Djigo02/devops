pipeline {
    agent any

    tools {
      maven 'maven:3.9.6'
      git 'Default'
    }

    stages {
        stage('Git') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/Djigo02/devops.git'
            }
        }
        stage('maven validate') {
            steps {
                 script {
                    sh 'mvn validate'
                }
            }
        }
        stage('maven compile') {
            steps {
                 script {
                    sh 'mvn compile'
                }
            }
        }
        stage('maven clean') {
            steps {
                 script {
                    sh 'mvn clean'
                }
            }
        }
    }
}
