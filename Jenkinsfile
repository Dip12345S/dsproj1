pipeline {
    agent any
    stages {
        stage('Clean Up') {
            steps {
                deleteDir()
            }
        }
        stage('Clone Repo') {
            steps {
                sh "git clone https://github.com/Dip12345S/myproj.git"
            }
        }
        stage('Test') {
            agent { dockerfile true }
            steps {
                sh 'echo Testing......>'
				sh 'python --version'
            }
        }        
    }
}