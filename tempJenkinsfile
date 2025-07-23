pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Siriivalli/talend-cdc-job.git'
            }
        }
        stage('Run Talend CDC Job') {
            steps {
                echo "▶ Running Talend job..."
                bat 'CDC_Project_run.bat'
            }
        }
    }
}  