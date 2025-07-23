pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Siriivalli/talend-cdc-job.git'
            }
        }
        stage('Run Talend Job') {
            steps {
                dir('CDC_Project') {
                    bat 'CDC_Project_run.bat'
                }
            }
        }
    }
}
