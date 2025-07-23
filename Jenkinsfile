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
                script {
                    // If CDC_Project_run.bat is inside CDC_Project folder
                    bat """
                        cd CDC_Project
                        CDC_Project_run.bat
                    """
                }
            }
        }
    }
}
