pipeline {
agent any

stages {
    stage('Use Custom Node.js') {
        steps {
            script {
                def nodeHome = tool(
                    name: 'NodeJS',
                    type: 'com.cloudbees.jenkins.plugins.customtools.CustomTool'
                )

                withEnv(["PATH+NODEJS=${nodeHome}\\node"]) {
                    bat 'node --version'
                    bat 'npm --version'
                }
            }
        }
    }
}

}
