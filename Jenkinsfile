pipeline {
    agent any
    triggers {
       githubPush()
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh """
                    ./gradlew clean build
                """
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                gradlew test
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}