pipeline {
    agent any
    stages {
        stage('Run Python job') {
            steps {
		sh '''
                  python3 /var/lib/jenkins/workspace/webhook_auroralabs_main/main.py 
		   '''
            }
        }
    }
}



