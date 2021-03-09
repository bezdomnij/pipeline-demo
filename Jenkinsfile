pipeline {
    agent any
    
    stages {
        stage ("Build") {
            steps {
                sh "which java"
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