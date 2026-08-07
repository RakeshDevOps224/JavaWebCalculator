pipeline{
    agent any
    stages{
        stage('1. checkout code'){
            steps{
                echo 'checkout code from the source code'
                git branch : 'master' ,
                credentialsId : 'gitHub_cred' ,
                url : 'https://github.com/RakeshDevOps224/JavaWebCalculator.git '
            }
        } 

        stage('2.compile the code'){
             
           steps{
            echo 'compile the source code '
            sh 'mvn compile'

            }
        }   

        stage('3. Test the code'){
           steps{
           echo 'Test the code run all the test case to pass '
           sh 'mvn Test'
           } 
 
       
        }       
       stage('4.File scan (trivy)'){
           steps{
           echo 'Trivy scanning the project object check vulnerabilities'
           sh 'trivy fs --format table -o .'
           }
       
        }
     }  
 }
