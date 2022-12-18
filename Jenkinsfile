pipeline {
    agent any
    tools {
        go 'go-1.19'
    }
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        disableConcurrentBuilds()
        skipDefaultCheckout()
    }
    stages {
        stage('Clean up') { 
            steps {
                deleteDir()
            }
        }
        stage('Clone') {
            steps {
                git credentialsId: '4f8dcf06-a320-4afd-914d-d7fa62be287c', url: 'git@github.com:ddrobnjak/go-simple-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'go build -o my-go-app main.go'
                sh 'ls -l'
            }
        }
        post {
            success {
                archiveArtifacts artifacts: '/', followSymlinks: false
        } 
    }       
    }
}
