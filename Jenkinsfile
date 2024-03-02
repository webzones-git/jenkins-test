pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your version control system
                git 'https://github.com/webzones-git/jenkins-test'
            }
        }
        
        stage('Install dependencies') {
            steps {
                // Install Python dependencies using pip
                //sh 'python3 -m pip install -r requirements.txt'
                sh 'pip install -r requirements.txt'
            }
        }
        
        stage('Run tests') {
            steps {
                // Run your Python tests
                sh 'python3 -m unittest discover -s tests -p ".py"'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your Python application
                sh 'python3 HelloWorld.py'
            }
        }
    }

}
