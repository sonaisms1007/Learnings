pipeline {
    agent any

    stages {
        stage('CheckOut') {
            steps {
                checkout scmGit(branches: [[name: '*/develop']], extensions: [], userRemoteConfigs: [[credentialsId: 'GitHub-Token', url: 'https://github.com/sonaisms1007/Learnings.git']])
            }
        }
    }
}
