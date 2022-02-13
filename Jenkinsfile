pipeline {
    agent any
    triggers {
       githubPush()
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh """
                    ./gradlew clean test
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