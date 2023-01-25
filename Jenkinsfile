pipeline {
    
    agent any

    triggers {
        pollSCM '* * * * *'
    }

    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                sleep 5
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Test') {
            steps {
                echo 'Hello Test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Hello Deploy'
            }
        }
    }
}