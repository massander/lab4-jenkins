pipeline {
    agent any

    environment {
        // Define the Python environment
        PYTHON_ENV = 'python3' // Or 'python' depending on the environment setup
    }

    stages {
        // stage('Checkout') {
        //     steps {
        //         // Pull the latest code from Git
        //         git branch: 'main', url: 'https://github.com/your-repo/python-app.git'
        //     }
        // }

        stage('Check Version') {
            steps {
                sh "${PYTHON_ENV} --version"
            }
        }

        stage('Run Unit Tests') {
            steps {
                // Run the unit tests using pytest or unittest
                sh "${PYTHON_ENV} -m unittest app_test.py"
            }
        }


    }
}
