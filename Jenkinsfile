pipeline {
    agent any

    stages {
        stage('Checkout Code from SCM') {
            steps {
                echo 'Checking out code from SCM'

                git branch: 'master',
                    credentialsId: 'github_cred',
                    url: 'https://github.com/RakeshDevOps224/JavaWebCalculator.git'
            }
        }
         stage('mvn build'){
             steps {
                echo 'Building the applicatio'
                sh 'mvn clean package'
                  }
            }
       }
    }

                        

