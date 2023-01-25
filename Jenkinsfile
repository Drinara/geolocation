pipeline {
    
    agent any

    triggers {
        pollSCM '* * * * *'
    }
    tools{
        maven 'M2_HOME'
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
        
        stage('Deploy') {
            steps {
                echo 'Hello Deploy'
            }
        }
    }
}