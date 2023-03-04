pipeline {
    agent any
    stages {
        stage('Run Python job') {
            steps {
		sh '''
                  python3 /var/jenkins_home/workspace/webhook_auroralabs/main.py 
		   '''
            }
        }
    }
}



