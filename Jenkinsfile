pipeline {
    agent any
    tools {nodejs "NODEJS"}
    stages {
        stage('Build') {
            steps {
                // Use 'bat' for Windows batch commands instead of 'sh'
                bat 'npm install'
            }
        }
        stage('Deliver') {
            steps {
                // Use 'bat' for Windows, adjust chmod command for Windows compatibility
                // 'chmod' doesn't work on Windows, but you might not need it if permissions are fine
                bat 'jenkins\\scripts\\deliver.bat'
                bat 'jenkins\\scripts\\kill.bat'
            }
        }
    }
}
