pipeline {
    agent any

    tools {
        gradle 'Gradle_3'
    }
    
    stages {
        stage('checkout SCM') {
            steps {
            git branch: 'main', url: "https://github.com/mohammedtwahamd/minimal.git"
            }
        }

        stage('Build') {
            steps {
                sh 'gradle build'
            }

        }

        stage('publish artifacts') {
            steps{
                sh 'gradle artifactoryPublish'
            }
        }
    }
}
