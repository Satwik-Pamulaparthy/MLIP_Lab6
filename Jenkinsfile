pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                echo 'Python is not compiled, but we could build packages here if needed.'
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo 'Creating virtual environment and installing dependencies...'
                python3 -m venv venv
                . venv/bin/activate
                pip install --upgrade pip
                pip install pytest numpy pandas scikit-learn
                echo 'Running tests...'
                pytest
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'In this step, we could deploy the project (optional for lab).'
            }
        }
    }
}
