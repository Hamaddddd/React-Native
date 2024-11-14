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
                // If htmlhint is installed, validate HTML (e.g., "htmlhint index.html")
                // Replace this line with any validation tool you have
                bat 'echo No HTML validation tool installed'
            }
        }
    }
}
