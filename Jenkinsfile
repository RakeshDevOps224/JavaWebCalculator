pipeline{
  agent any
  stages{
    stage('check out code from scm'){
       step{
         echo 'scm tool checkout code' 
         git branch : 'master ',
         credentialId : 'credentials_GitHub', 
         url : 'https://github.com/RakeshDevOps224/JavaWebCalculator.git'
}

}

}
}
