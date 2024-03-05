pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out the code from your version control system (e.g., Git)
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    // Set up a Python environment
                    def pythonVersion = '3.9'
                    def pythonHome = tool name: "Python${pythonVersion}", type: 'hudson.plugins.python.PythonInstallation'
                    env.PATH = "${pythonHome}\\Scripts;${env.PATH}"

                    // Install dependencies (if needed)
                   // bat 'pip install -r requirements.txt'  // Replace with your requirements file

                    // Run the Python script
                    bat 'python hello.py'  // Replace with the actual name of your Python script
                }
            }
        }

        // Add more stages as needed (e.g., testing, deployment)
    }

    post {
        always {
            // Clean up or perform any necessary actions after the pipeline execution
        }
    }
}
