pipeline {
    agent any

    stages{
        stage("create zip file"){
            steps{
               
           sh 'zip mdwScript-$(date +%y%m%d-%H%M%S).zip *  --exclude Jenkinsfile README.md '  
            
            }
        }
        
    }
}
