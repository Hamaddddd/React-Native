pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/Hamaddddd/React-Native.git',
                branch: 'main', 
                credentialsId: 'github-pat'
            }
        }
        stage('Build Website') {
            steps {
                // Run the build script (hello.bat)
                bat './hello.bat'
            }
        }
        stage('HTML Validation') {
            steps {
                echo 'Running HTML Validation...'
                // Run htmlhint to validate HTML files
                bat 'htmlhint index.html || echo "HTML issues detected!"'
            }
        }
    }
}
