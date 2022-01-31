pipeline {
    agent any
    stages {
        stage('clone repo') {
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/hienpham4194/my-app.git"
                sh "mvn clean -f my-app"
            }
        }
        stage('install') {
            steps {
                sh "mvn install -f my-app"
            }
        }
        stage('test') {
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage('package') {
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
