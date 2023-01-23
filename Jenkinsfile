pipeline {
    agent any

    stages{
        stage("create zip file"){
            steps{
               
           sh 'zip mdwScript-$(date +%d%m%y-%H%M%S).zip *  --exclude Jenkinsfile README.md '  
            
            }
        }
        
	stage('Build') {
            steps {
                // Build steps here
            }
        }
    
    post {
        success {
            slackSend color: 'good', message: 'Build succeeded!'
        }
        failure {
            slackSend color: 'danger', message: 'Build failed!'
        }

    }
  }
}
