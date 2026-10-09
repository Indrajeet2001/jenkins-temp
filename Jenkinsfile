pipeline {
    agent any

    tools{
        jdk 'JAVA-17'
    }

    stages {
        stage('Verify Java') {
            steps {
                bat 'java -version'
                bat 'javac -version'
                bat 'echo JAVA_HOME is set to %JAVA_HOME%'
            }
        }

        stage('Build') {
            steps {
                echo 'Java is ready for the build!'
            }
        }
    }

    post {
        success {
            echo 'JDK setup and verification completed successfully.'
        }
        failure {
            echo 'JDK setup or verification failed.'
        }
    }
}
