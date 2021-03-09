pipeline {
    agent any
    
    stages {
        stage ("Build") {
            steps {
                sh "readlink -f $(which java)"
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