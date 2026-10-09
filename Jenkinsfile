pipeline {

agent any

stages {

stage('Build') {

steps {

echo 'Building the project....

bat 'echo Build completed successfully!'

}

}

stage('Test') {

steps {

echo 'Running tests....'

bat 'echo Tests passed!'

}

}

}

stage('Deploy') {

}

steps {

echo 'Deploying the application...'

bat 'echo Deployment completed!'

post {

success {

}

echo 'Pipeline completed successfully!"

failure {

echo 'Pipeline falled.'
}

}
}