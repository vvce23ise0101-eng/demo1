pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {
        stage('CHECKOUT') {
            steps {
                git 'https://github.com/vvce23ise0101-eng/demo1.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }
    }
}