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
                sh '/Applications/apache-maven-3.6.3/bin/mvn -version' 
            }
        }
	    
	stage('Slack it'){
            steps {
                slackSend channel: '#devops', 
                          message: 'Hello, world'
            }
        }
    }
}
