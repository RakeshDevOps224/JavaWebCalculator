pipeline{
    agent any
    stages{
        stage('1. checkout code'){
            steps{
                echo 'checkout code from the source code'
                git branch : 'master' ,
                credentialsId : 'gitHub_cred' ,
                url : ''
            }
        }
    }
}
