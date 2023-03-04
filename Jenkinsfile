pipeline {
    agent any
    stages {
        stage('Run Python job') {
            steps {
		sh '''
                   python /app/my_python_script.py
		   '''
            }
        }
    }
}

