pipeline {
    agent any
    tools {nodejs "NODEJS"}
    stages {
        stage('Build') {
            steps {
                // Use 'bat' for Windows batch commands instead of 'sh'
                bat 'npm install'
                // Build the Angular project and store the output in the custom location
                bat 'npm run ng build'
            }
        }
        stage('Deliver') {
            steps {
                // Use 'bat' for Windows to move files if necessary
                // In this example, let's assume you want to move the build files somewhere else
                bat 'move dist\\custom-location C:\\Users\\sridhar\\Desktop\\air'

                // Run your delivery script (e.g., to deploy or perform further actions)
                bat 'jenkins\\scripts\\kill.bat'
            }
        }
    }
}
