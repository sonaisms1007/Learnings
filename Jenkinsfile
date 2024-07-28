pipeline {
    agent any

    stages {
        stage('CheckOut') {
            steps {
                checkout scmGit(branches: [[name: '*/develop']], extensions: [], userRemoteConfigs: [[credentialsId: 'GitHub-Token', url: 'https://github.com/sonaisms1007/Learnings.git']])
            }
        }
		 stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
		 stage('Publish') {
            steps {
				echo "publish to the Artifactory"
             }
        }
		stage('Deploy') {
            steps {	
                echo "Deployed"
            }
        }
    }
}
