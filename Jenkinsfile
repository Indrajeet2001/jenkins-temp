pipeline {
    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT', 
            choices: ['DEV', 'TEST', 'PROD'], 
            description: 'Select the environment to deploy to'
        )
    }

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

        stage('Test'){
            steps {
                bat "echo Running automates tests..."
            }
        }

        stage('Deploy to DEV'){
            when {
                expression { return params.ENVIRONMENT == 'DEV' }
            }
            steps {
                echo "Deploying to DEV environment..."
            }
        }

        stage('Deploy to TEST') {
            when {
                expression { return params.ENVIRONMENT == 'TEST' }
            }
            steps {
                echo "Deploying to TEST environment..."
            }
        }

        stage('Deploy to PROD') {
            when {
                expression { return params.ENVIRONMENT == 'PROD' }
            }
            steps {
                input message: "Are you sure you want to deploy to PROD?", 
                ok: "Apporve"

                echo "Deploying to PROD environment..."
            }
        }  

    }
}