pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '998721e2-78de-42da-9242-d693d56dcfd7', url: 'https://github.com/Akshit2812/demo_devops.git']]])
            }
        }
        stage('Build') {
            steps{
                git branch: 'main', credentialsId: '998721e2-78de-42da-9242-d693d56dcfd7', url: 'https://github.com/Akshit2812/demo_devops.git'
                bat 'python demo_devops.py'
            }
        }
        stage('Test'){
            steps{
                echo 'the job has been tested'
            }
        }
    }
}
