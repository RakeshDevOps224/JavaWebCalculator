pipeline {
    agent any

    stages {

        stage('1. Checkout Code') {
            steps {
                echo 'Checkout code from GitHub'
                git branch: 'master',
                    credentialsId: 'gitHub_cred',
                    url: 'https://github.com/RakeshDevOps224/JavaWebCalculator.git'
            }
        }

        stage('2. Compile Code') {
            steps {
                echo 'Compiling the source code'
                sh 'mvn compile'
            }
        }

        stage('3. Test Code') {
            steps {
                echo 'Running test cases'
                sh 'mvn test'
            }
        }

        stage('4. File System Scan (Trivy)') {
            steps {
                echo 'Scanning project files using Trivy'
                sh  'trivy fs --format table -o trivy-report.txt' .
            }
        }
    }
}
