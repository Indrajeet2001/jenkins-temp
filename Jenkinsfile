pipeline {
agent any

stages {
    stage('Show Parameters') {
        steps {
            echo "Selected Environment: ${params.ENVIRONMENT}"
            echo "Run tests: ${params.RUN_TESTS}"
        }
    }

    stage ("Build") {
        steps {
            echo "Building the project..."
        }
    }

    stage('Test') {
        steps {
            bat 'echo Running tests...'  
        }
    }

    stage('Deploy') {
        steps {
            echo "Deploying to ${params.ENVIRONMENT} environment..."
        }
}

}
