pipeline {
    agent any

    stages{
        stage("create zip file"){
            steps{
               
           sh 'zip mdwScript-$(date +%d%m%y-%H%M%S).zip *  --exclude Jenkinsfile README.md '  
            
	    slackSend channel: 'DevOps-Team', message: 'New job has been build'
            }
        }
        
    }
}
