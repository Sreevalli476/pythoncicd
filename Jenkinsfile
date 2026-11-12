pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test') {
            steps {
              
                bat 'python -c "import app"'
            }
        }

        stage('Package') {
            steps {
               
                bat 'python -m py_compile app.py'
                bat 'tar -cf app.tar app.py'
            }
        }
    }
}