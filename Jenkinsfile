pipeline {
    agent any // Specifies that the pipeline can run on any available agent
    stages {
        stage('run-parallel-branches') {
          steps {
            parallel(
              a: {
                sh 'echo "Building the application..."' // Executes a shell command
              },
              b: {
                sh 'echo "Running tests..."'
              }
            )
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
