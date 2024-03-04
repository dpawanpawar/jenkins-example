pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Assuming you are using Git for version control
                checkout scm
            }
        }

        stage('Check Python Version') {
            steps {
                script {
                    // Run a Windows command to check Python version
                    def pythonVersion = bat(script: 'py -3 --version 2>&1', returnStatus: true)

                    if (pythonVersion == 0) {
                        echo "Python Version: $($pythonVersion)"
                        
                        // You can add conditions based on the Python version if needed
                        if ($pythonVersion.contains('3.')) {
                            echo "This job requires Python 3."
                        } else {
                            error "Unsupported Python version."
                        }
                    } else {
                        error "Error checking Python version."
                    }
                }
            }
        }

        // Add more stages as needed for your build process
        // ...

    }


