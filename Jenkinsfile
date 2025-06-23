pipeline {
    agent any

    environment {
        PYTHON_SCRIPT = "app.py"
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out source code from GitHub..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Build step (if any)..."
                // No real build needed for this example
            }
        }

        stage('Run Script') {
            steps {
                echo "Running Python script..."
                sh "user/bin/python3 app.py"
            }
        }

        stage('Test') {
            steps {
                echo "Running basic test..."
            }
        }
    }

    post {
        success {
            echo "Pipeline finished successfully!"
        }
        failure {
            echo "Pipeline failed ❌"
        }
    }
}
