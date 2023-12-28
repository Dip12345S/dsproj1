pipeline {
    agent any
    stages {
        stage('Checkout with Version Control') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Dip12345S/dsproj1.git']])
            }
        }
        stage('Built Docker Image') {
            steps {
                script{
                    sh 'docker built -t dsproj1 .'
                }
            }
        }
    }
}