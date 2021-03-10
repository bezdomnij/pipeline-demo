pipeline {
    agent any

    tools {
        maven "3.6.3"
    }
    
    stages {
        stage ("Build") {
            steps {
                sh "which java"
                sh "which javac"
                sh "java -version"
                sh "javac -version"
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}