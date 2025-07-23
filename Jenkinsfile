pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Siriivalli/talend-cdc-job.git'
            }
        }
        stage('Debug - List Files') {
            steps {
                echo "📂 Listing repo root files..."
                bat 'dir'
                
                echo "📂 Listing CDC_Project folder (if it exists)..."
                bat 'if exist CDC_Project (dir CDC_Project) else echo CDC_Project folder NOT FOUND'
            }
        }
    }
}
