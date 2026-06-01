pipeline {

    agent any

    tools {
        maven 'Maven3'
    }

    triggers {
        githubPush()
    }

    stages {

        stage('Build') {

            steps {

                sh 'mvn clean package'

            }
        }

        stage('Archive Artifact') {

            steps {

                archiveArtifacts artifacts: 'target/*.war'

            }
        }
    }
}
