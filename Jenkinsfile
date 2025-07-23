pipeline {
    agent any
    
    stages {
        stage('Checkout from GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/Siriivalli/talend-cdc-job.git'
            }
        }
        
        stage('Run Talend CDC Job') {
            steps {
                script {
                    // Windows Jenkins agent
                    bat 'CDC_Project_0.1.bat'
                    
                    // If Linux Jenkins agent:
                    // sh './CDC_Project_0.1.sh'
                }
            }
        }
    }
}
