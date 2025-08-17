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
            when {
                branch 'main' // This stage only runs when the branch is 'main'
            }
            steps {
                sh 'echo "Deploying the application..."'
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
