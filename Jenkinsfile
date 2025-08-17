pipeline {
    agent any // Specifies that the pipeline can run on any available agent

    stages {
        stage('Build') { // Defines a stage named 'Build'
            steps {
                sh 'echo "Building the application..."' // Executes a shell command
            }
        }

        stage('Test') { // Defines a stage named 'Test'
            steps {
                sh 'echo "Running tests..."'
            }
        }

        stage('Deploy') { // Defines a stage named 'Deploy'
            steps {
                sh 'echo "Deploying the application..."'
            }
        }
        stage('Consolidate Results') { // Defines a stage named 'Deploy'
            steps {
                input('Do you want to capture results?')
                sh 'echo "Consolidating Results..."'
            }
        }
    }

    post { // Defines post-build actions
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
