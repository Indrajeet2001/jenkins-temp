pipeline {
    agent any


    stages {
        stage('Use Jenkins Java 17 ') {            
            tools{
                jdk 'JAVA-17'
            }
            steps {
                echo 'Using Jenkins managed Java 17.'
                bat 'java -version'
                bat 'echo JAVA_HOME is set to %JAVA_HOME%'
            }
        }

        stage('Using system Java 21') {
            steps {
                echo 'Using system-installed java '
                bat '"C:\\Program Files\\Eclipse Adoptium\\jdk-21.0.12.101-hotspot\\bin\\java.exe" -version'
            }
        }

        stage('Use Jenkins Java Again =')
        {
            tools{
                jdk 'JAVA-17'
            }
            steps {
                bat 'java -version'
            }
        }
    }

   
}
