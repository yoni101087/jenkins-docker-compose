pipeline {
    agent any
    stages {
        stage('Run Python job') {
            steps {
		sh '''
                   echo "print("Devops is great")")" > my_python_script.py
                   python my_python_script.py
		   '''
            }
        }
    }
}

