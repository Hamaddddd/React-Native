pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git url: 'https://github.com/your-username/jenkins-website-ci.git'
            }
        }
        stage('Build Website') {
            steps {
                // Run the build script, assumed to be "hello.sh"
                sh './hello.sh'
            }
        }
        stage('HTML Validation') {
            steps {
                // Validate HTML, assuming "tidy" is installed
                echo 'Running HTML Validation...'
                sh 'tidy -q -e index.html || echo "HTML issues detected!"'
            }
        }
    }
}
