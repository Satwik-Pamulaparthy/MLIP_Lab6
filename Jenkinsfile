pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                echo 'Python is not compiled, but we could build wheels or packages here if needed.'
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo 'Creating and activating virtual environment...'
                python3 -m venv venv
                . venv/bin/activate
                echo 'Installing dependencies...'
                pip install --upgrade pip
                pip install pytest numpy pandas scikit-learn
                echo 'Running tests with pytest...'
                pytest
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'In this step, we could deploy our project.'
                echo 'In your lab, this can stay as a placeholder.'
            }
        }
    }
}
