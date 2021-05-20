pipeline {
    agent {
	any {
    }
    }
    stages {
	stage(checkout){
	    steps {
		sh 'echo "checkout successfully thru token"'
	}
	}	
        stage('Build') { 
            steps {
                sh 'echo "build successfully thru mvn"' 
            }
        }
	    
	stage('Slack it'){
            steps {
                slackSend channel: '#devops', 
                          message: 'Hello, bitOrions'
            }
        }
    }
}
